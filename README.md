{
  "name": "tine-brain-player",
  "version": "1.0.0",
  "description": "Mobile-first education + entertainment app for children age 5+",
  "main": "index.js",
  "scripts": {
    "start": "expo start",
    "android": "expo start --android",
    "ios": "expo start --ios",
    "web": "expo start --web",
    "build-android": "eas build --platform android",
    "build-ios": "eas build --platform ios",
    "type-check": "tsc --noEmit"
  },
  "dependencies": {
    "expo": "~51.0.0",
    "expo-splash-screen": "~0.27.0",
    "expo-status-bar": "~1.12.0",
    "expo-font": "~12.0.0",
    "expo-av": "~14.0.0",
    "expo-haptics": "~13.0.0",
    "react": "18.3.1",
    "react-native": "0.74.5",
    "react-native-reanimated": "~3.15.0",
    "react-native-gesture-handler": "~2.14.0",
    "react-native-safe-area-context": "4.8.2",
    "react-native-screens": "~3.31.0",
    "react-navigation": "^6.1.9",
    "react-navigation-native-stack": "^6.9.14",
    "react-navigation-bottom-tabs": "^6.5.8",
    "zustand": "^4.4.0",
    "expo-sqlite": "~14.0.0",
    "uuid": "^9.0.1",
    "react-native-svg": "15.2.0"
  },
  "devDependencies": {
    "@babel/core": "^7.24.0",
    "@types/react": "~18.2.45",
    "@types/react-native": "^0.74.0",
    "@types/uuid": "^9.0.7",
    "typescript": "~5.3.3"
  },
  {
  "compilerOptions": {
    "target": "ES2020",
    "useDefineForClassFields": true,
    "lib": ["ES2020", "DOM", "DOM.Iterable"],
    "module": "ESNext",
    "skipLibCheck": true,
    "esModuleInterop": true,
    "allowSyntheticDefaultImports": true,
    "strict": true,
    "resolveJsonModule": true,
    "isolatedModules": true,
    "jsx": "react-jsx",
    "moduleResolution": "bundler",
    "allowImportingTsExtensions": true,
    "forceConsistentCasingInFileNames": true,
    "noEmit": true,
    "types": ["react", "react-native", "@types/uuid"]
  },
  "include": ["src"],
  "exclude": ["node_modules"],
  "ts-node": {
    "compilerOptions": {
      "module": "commonjs"
    }
  }
}

{
  "expo": {
    "name": "Tine Brain Player",
    "slug": "tine-brain-player",
    "version": "1.0.0",
    "orientation": "portrait",
    "userInterfaceStyle": "light",
    "assetBundlePatterns": ["**/*"],
    "ios": {
      "supportsTabletMode": true,
      "bundleIdentifier": "com.tinebrainplayer.app"
    },
    "android": {
      "adaptiveIcon": {
        "foregroundImage": "./assets/adaptive-icon.png",
        "backgroundColor": "#FFFFFF"
      },
      "package": "com.tinebrainplayer.app",
      "minSdkVersion": 21
    },
    "web": {
      "favicon": "./assets/favicon.png"
    },
    "plugins": [
      [
        "expo-font",
        {
          "fonts": [
            "./assets/fonts/Poppins-Regular.ttf",
            "./assets/fonts/Poppins-Bold.ttf",
            "./assets/fonts/Poppins-SemiBold.ttf"
          ]
        }
      ]
    ],
    "splash": {
      "image": "./assets/splash.png",
      "resizeMode": "contain",
      "backgroundColor": "#FFFFFF"
    }
  }
}

module.exports = function (api) {
  api.cache(true);
  return {
    presets: ['babel-preset-expo'],
    plugins: ['react-native-reanimated/plugin'],
  };
};

# Expo
.expo/
dist/
.expo-shared/

# Node
node_modules/
npm-debug.*
.pnp
.pnp.js

# Testing
*.lcov
.nyc_output
coverage

# Misc
.DS_Store
*.pem
.env
.env.local
.env.*.local

# IDE
.idea
.vscode
*.swp
*.swo
*.swn
*~
*.orig

# Build
build/
dist/

# Cache
.eslintcache
.cache

/**
 * Soft pastel color palette for children's app
 * Clean, safe, and engaging for age 5+
 */

export const colors = {
  // Primary colors - soft pastels
  primary: '#FF6B9D',      // Soft pink
  primaryLight: '#FFB3D9',
  primaryDark: '#E84C7C',

  secondary: '#4ECDC4',    // Soft teal
  secondaryLight: '#A0F0ED',
  secondaryDark: '#2EAFA0',

  tertiary: '#FFE66D',     // Soft yellow
  tertiaryLight: '#FFF4B3',
  tertiaryDark: '#FFD700',

  accent: '#95E1D3',       // Soft mint green
  accentLight: '#D5F7F0',
  accentDark: '#5FBF9E',

  // Neutrals
  background: '#FFFFFF',
  surface: '#F8F9FA',
  surfaceAlt: '#F0F1F3',
  
  // Text colors
  text: '#2D3748',
  textSecondary: '#718096',
  textLight: '#A0AEC0',

  // Feedback colors
  success: '#48BB78',      // Green
  successLight: '#C6F6D5',
  error: '#F56565',        // Red
  errorLight: '#FED7D7',
  warning: '#ED8936',      // Orange
  warningLight: '#FEEBC8',

  // Game-specific colors
  star: '#FFD700',
  badge: '#FF6B9D',
  
  // Transparent variants
  overlay: 'rgba(45, 55, 72, 0.5)',
  overlayLight: 'rgba(45, 55, 72, 0.1)',
};

export type Colors = typeof colors;

/**
 * Typography system optimized for children
 * Large, readable, friendly fonts
 */

export const typography = {
  // Font families
  fontFamily: {
    regular: 'Poppins-Regular',
    medium: 'Poppins-SemiBold',
    bold: 'Poppins-Bold',
  },

  // Font sizes
  fontSize: {
    xs: 12,
    sm: 14,
    base: 16,
    lg: 18,
    xl: 20,
    '2xl': 24,
    '3xl': 28,
    '4xl': 32,
    '5xl': 40,
    '6xl': 48,
  },

  // Line heights
  lineHeight: {
    tight: 1.2,
    normal: 1.5,
    relaxed: 1.75,
    loose: 2,
  },
};

export type Typography = typeof typography;

/**
 * Consistent spacing system
 * Based on 8px baseline for clean alignment
 */

export const spacing = {
  xs: 4,
  sm: 8,
  md: 12,
  lg: 16,
  xl: 20,
  '2xl': 24,
  '3xl': 32,
  '4xl': 40,
  '5xl': 48,
  '6xl': 56,
  '7xl': 64,
};

export type Spacing = typeof spacing;

import { colors } from './colors';
import { typography } from './typography';
import { spacing } from './spacing';

export const theme = {
  colors,
  typography,
  spacing,
  
  // Border radius - soft corners for children's app
  borderRadius: {
    sm: 8,
    md: 12,
    lg: 16,
    xl: 24,
    full: 9999,
  },

  // Shadows - soft and subtle
  shadows: {
    sm: {
      shadowColor: '#000',
      shadowOffset: { width: 0, height: 2 },
      shadowOpacity: 0.1,
      shadowRadius: 4,
      elevation: 2,
    },
    md: {
      shadowColor: '#000',
      shadowOffset: { width: 0, height: 4 },
      shadowOpacity: 0.12,
      shadowRadius: 8,
      elevation: 4,
    },
    lg: {
      shadowColor: '#000',
      shadowOffset: { width: 0, height: 8 },
      shadowOpacity: 0.15,
      shadowRadius: 12,
      elevation: 6,
    },
  },
};

export type Theme = typeof theme;

/**
 * Global user state management using Zustand
 * Manages user progress, rewards, and app settings
 */

import { create } from 'zustand';

export interface UserProgress {
  totalStars: number;
  totalBadges: string[];
  dailyStreak: number;
  lastPlayDate: string;
  soundEnabled: boolean;
  musicEnabled: boolean;
  darkMode: boolean;
  language: 'en' | 'es' | 'fr';
}

interface UserStore extends UserProgress {
  addStars: (count: number) => void;
  addBadge: (badgeId: string) => void;
  incrementStreak: () => void;
  resetProgress: () => void;
  toggleSound: () => void;
  toggleMusic: () => void;
  toggleDarkMode: () => void;
  setLanguage: (lang: 'en' | 'es' | 'fr') => void;
  updateLastPlayDate: () => void;
}

const initialState: UserProgress = {
  totalStars: 0,
  totalBadges: [],
  dailyStreak: 0,
  lastPlayDate: new Date().toISOString().split('T')[0],
  soundEnabled: true,
  musicEnabled: true,
  darkMode: false,
  language: 'en',
};

export const useUserStore = create<UserStore>((set) => ({
  ...initialState,
  
  addStars: (count: number) =>
    set((state) => ({
      totalStars: state.totalStars + count,
    })),
  
  addBadge: (badgeId: string) =>
    set((state) => ({
      totalBadges: [...new Set([...state.totalBadges, badgeId])],
    })),
  
  incrementStreak: () =>
    set((state) => ({
      dailyStreak: state.dailyStreak + 1,
    })),
  
  resetProgress: () => set(initialState),
  
  toggleSound: () =>
    set((state) => ({
      soundEnabled: !state.soundEnabled,
    })),
  
  toggleMusic: () =>
    set((state) => ({
      musicEnabled: !state.musicEnabled,
    })),
  
  toggleDarkMode: () =>
    set((state) => ({
      darkMode: !state.darkMode,
    })),
  
  setLanguage: (lang: 'en' | 'es' | 'fr') =>
    set({
      language: lang,
    }),
  
  updateLastPlayDate: () =>
    set({
      lastPlayDate: new Date().toISOString().split('T')[0],
    }),
}));

/**
 * Game-specific state management
 * Tracks progress in individual games
 */

import { create } from 'zustand';

export interface GameProgress {
  gameId: string;
  gamesPlayed: number;
  completedLevels: number;
  highScore: number;
  lastPlayed: string;
}

interface GameStore {
  gameProgress: Map<string, GameProgress>;
  updateGameProgress: (gameId: string, progress: Partial<GameProgress>) => void;
  getGameProgress: (gameId: string) => GameProgress | undefined;
  resetGameProgress: (gameId: string) => void;
}

export const useGameStore = create<GameStore>((set, get) => ({
  gameProgress: new Map(),
  
  updateGameProgress: (gameId: string, progress: Partial<GameProgress>) =>
    set((state) => {
      const newMap = new Map(state.gameProgress);
      const existing = newMap.get(gameId) || {
        gameId,
        gamesPlayed: 0,
        completedLevels: 0,
        highScore: 0,
        lastPlayed: new Date().toISOString(),
      };
      newMap.set(gameId, { ...existing, ...progress });
      return { gameProgress: newMap };
    }),
  
  getGameProgress: (gameId: string) => get().gameProgress.get(gameId),
  
  resetGameProgress: (gameId: string) =>
    set((state) => {
      const newMap = new Map(state.gameProgress);
      newMap.delete(gameId);
      return { gameProgress: newMap };
    }),
}));

/**
 * SQLite database schema for Tine Brain Player
 */

export const DATABASE_NAME = 'tine_brain_player.db';

export const SCHEMA = `
-- User Progress Table
CREATE TABLE IF NOT EXISTS user_progress (
  id TEXT PRIMARY KEY,
  total_stars INTEGER DEFAULT 0,
  daily_streak INTEGER DEFAULT 0,
  last_play_date TEXT,
  sound_enabled INTEGER DEFAULT 1,
  music_enabled INTEGER DEFAULT 1,
  dark_mode INTEGER DEFAULT 0,
  language TEXT DEFAULT 'en',
  created_at TEXT,
  updated_at TEXT
);

-- Game Progress Table
CREATE TABLE IF NOT EXISTS game_progress (
  id TEXT PRIMARY KEY,
  game_id TEXT NOT NULL,
  games_played INTEGER DEFAULT 0,
  completed_levels INTEGER DEFAULT 0,
  high_score INTEGER DEFAULT 0,
  last_played TEXT,
  created_at TEXT,
  updated_at TEXT,
  UNIQUE(game_id)
);

-- Badges/Achievements Table
CREATE TABLE IF NOT EXISTS badges (
  id TEXT PRIMARY KEY,
  badge_id TEXT NOT NULL,
  earned_at TEXT,
  created_at TEXT
);

-- Planner Tasks Table
CREATE TABLE IF NOT EXISTS planner_tasks (
  id TEXT PRIMARY KEY,
  task_name TEXT NOT NULL,
  is_completed INTEGER DEFAULT 0,
  completed_date TEXT,
  created_at TEXT,
  updated_at TEXT
);

-- Word Puzzle Progress
CREATE TABLE IF NOT EXISTS word_puzzle_progress (
  id TEXT PRIMARY KEY,
  level INTEGER NOT NULL,
  word TEXT NOT NULL,
  attempts INTEGER DEFAULT 0,
  completed INTEGER DEFAULT 0,
  completed_at TEXT,
  created_at TEXT,
  updated_at TEXT
);

-- Color by Number Progress
CREATE TABLE IF NOT EXISTS color_by_number_progress (
  id TEXT PRIMARY KEY,
  template_id TEXT NOT NULL,
  completed INTEGER DEFAULT 0,
  completed_at TEXT,
  time_spent INTEGER DEFAULT 0,
  created_at TEXT,
  updated_at TEXT
);

-- Memory Match Progress
CREATE TABLE IF NOT EXISTS memory_match_progress (
  id TEXT PRIMARY KEY,
  difficulty TEXT NOT NULL,
  pairs_found INTEGER DEFAULT 0,
  total_moves INTEGER DEFAULT 0,
  completed INTEGER DEFAULT 0,
  completed_at TEXT,
  time_spent INTEGER DEFAULT 0,
  created_at TEXT,
  updated_at TEXT
);

-- Create indexes for better query performance
CREATE INDEX IF NOT EXISTS idx_game_progress_game_id ON game_progress(game_id);
CREATE INDEX IF NOT EXISTS idx_planner_tasks_date ON planner_tasks(completed_date);
CREATE INDEX IF NOT EXISTS idx_badges_earned_at ON badges(earned_at);
`;

/**
 * Database initialization and management
 * Using expo-sqlite for local data persistence
 */

import * as SQLite from 'expo-sqlite';
import { DATABASE_NAME, SCHEMA } from './schema';

let db: SQLite.SQLiteDatabase | null = null;

/**
 * Initialize database connection
 */
export const initializeDatabase = async (): Promise<SQLite.SQLiteDatabase> => {
  if (db) {
    return db;
  }

  try {
    db = await SQLite.openDatabaseAsync(DATABASE_NAME);
    
    // Enable foreign keys
    await db.execAsync('PRAGMA foreign_keys = ON');
    
    // Execute schema
    await db.execAsync(SCHEMA);
    
    console.log('✓ Database initialized successfully');
    return db;
  } catch (error) {
    console.error('✗ Database initialization failed:', error);
    throw error;
  }
};

/**
 * Get database instance
 */
export const getDatabase = async (): Promise<SQLite.SQLiteDatabase> => {
  if (!db) {
    return initializeDatabase();
  }
  return db;
};

/**
 * Execute a query
 */
export const executeQuery = async (
  sql: string,
  params: any[] = []
): Promise<any[]> => {
  const database = await getDatabase();
  return database.getAllAsync(sql, params);
};

/**
 * Execute a single result query
 */
export const executeSingleQuery = async (
  sql: string,
  params: any[] = []
): Promise<any | null> => {
  const database = await getDatabase();
  return database.getFirstAsync(sql, params);
};

/**
 * Execute an insert/update/delete
 */
export const executeWrite = async (
  sql: string,
  params: any[] = []
): Promise<SQLite.SQLiteRunResult> => {
  const database = await getDatabase();
  return database.runAsync(sql, params);
};

/**
 * Close database connection
 */
export const closeDatabase = async (): Promise<void> => {
  if (db) {
    await db.closeAsync();
    db = null;
  }
};

/**
 * Reusable Button component
 * Large touch targets for children
 */

import React from 'react';
import {
  TouchableOpacity,
  Text,
  StyleSheet,
  ViewStyle,
} from 'react-native';
import { theme } from '../theme';

interface ButtonProps {
  label: string;
  onPress: () => void;
  variant?: 'primary' | 'secondary' | 'tertiary' | 'success';
  size?: 'sm' | 'md' | 'lg';
  disabled?: boolean;
  style?: ViewStyle;
}

const Button: React.FC<ButtonProps> = ({
  label,
  onPress,
  variant = 'primary',
  size = 'lg',
  disabled = false,
  style,
}) => {
  const variantStyles = {
    primary: {
      backgroundColor: theme.colors.primary,
      borderColor: theme.colors.primaryDark,
    },
    secondary: {
      backgroundColor: theme.colors.secondary,
      borderColor: theme.colors.secondaryDark,
    },
    tertiary: {
      backgroundColor: theme.colors.tertiary,
      borderColor: theme.colors.tertiaryDark,
    },
    success: {
      backgroundColor: theme.colors.success,
      borderColor: theme.colors.success,
    },
  };

  const sizeStyles = {
    sm: { paddingVertical: theme.spacing.md, paddingHorizontal: theme.spacing.lg },
    md: { paddingVertical: theme.spacing.lg, paddingHorizontal: theme.spacing.xl },
    lg: { paddingVertical: theme.spacing.xl, paddingHorizontal: theme.spacing['2xl'] },
  };

  const sizeTextStyles = {
    sm: { fontSize: theme.typography.fontSize.base },
    md: { fontSize: theme.typography.fontSize.lg },
    lg: { fontSize: theme.typography.fontSize.xl },
  };

  return (
    <TouchableOpacity
      style={[
        styles.button,
        variantStyles[variant],
        sizeStyles[size],
        disabled && styles.disabled,
        style,
      ]}
      onPress={onPress}
      disabled={disabled}
      activeOpacity={0.7}
    >
      <Text
        style={[
          styles.text,
          sizeTextStyles[size],
          disabled && styles.disabledText,
        ]}
      >
        {label}
      </Text>
    </TouchableOpacity>
  );
};

const styles = StyleSheet.create({
  button: {
    borderRadius: theme.borderRadius.xl,
    alignItems: 'center',
    justifyContent: 'center',
    borderWidth: 2,
    ...theme.shadows.md,
  },
  text: {
    fontFamily: theme.typography.fontFamily.bold,
    color: theme.colors.background,
    textAlign: 'center',
  },
  disabled: {
    opacity: 0.5,
  },
  disabledText: {
    color: theme.colors.textLight,
  },
});

export default Button;

/**
 * App header component
 * Shows title and user stats
 */

import React from 'react';
import { View, Text, StyleSheet } from 'react-native';
import { theme } from '../theme';

interface HeaderProps {
  title: string;
  stars?: number;
  showStats?: boolean;
}

const Header: React.FC<HeaderProps> = ({
  title,
  stars = 0,
  showStats = true,
}) => {
  return (
    <View style={styles.header}>
      <Text style={styles.title}>{title}</Text>
      {showStats && (
        <View style={styles.statsContainer}>
          <Text style={styles.star}>⭐</Text>
          <Text style={styles.starsText}>{stars}</Text>
        </View>
      )}
    </View>
  );
};

const styles = StyleSheet.create({
  header: {
    flexDirection: 'row',
    justifyContent: 'space-between',
    alignItems: 'center',
    paddingHorizontal: theme.spacing.lg,
    paddingVertical: theme.spacing.lg,
    backgroundColor: theme.colors.background,
    borderBottomColor: theme.colors.surface,
    borderBottomWidth: 1,
  },
  title: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize['2xl'],
    color: theme.colors.text,
  },
  statsContainer: {
    flexDirection: 'row',
    alignItems: 'center',
    gap: theme.spacing.xs,
    backgroundColor: theme.colors.surface,
    paddingHorizontal: theme.spacing.md,
    paddingVertical: theme.spacing.sm,
    borderRadius: theme.borderRadius.full,
  },
  star: {
    fontSize: 20,
  },
  starsText: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize.base,
    color: theme.colors.text,
  },
});

export default Header;

/**
 * Game category card for home screen
 * Large, colorful, touchable cards
 */

import React from 'react';
import {
  TouchableOpacity,
  Text,
  StyleSheet,
  View,
} from 'react-native';
import { theme } from '../theme';

interface GameCardProps {
  title: string;
  icon: React.ReactNode;
  color: string;
  onPress: () => void;
  badge?: string;
}

const GameCard: React.FC<GameCardProps> = ({
  title,
  icon,
  color,
  onPress,
  badge,
}) => {
  return (
    <TouchableOpacity
      style={[styles.card, { backgroundColor: color }]}
      onPress={onPress}
      activeOpacity={0.8}
    >
      <View style={styles.iconContainer}>{icon}</View>
      <Text style={styles.title}>{title}</Text>
      {badge && <View style={styles.badgeContainer}>
        <Text style={styles.badgeText}>{badge}</Text>
      </View>}
    </TouchableOpacity>
  );
};

const styles = StyleSheet.create({
  card: {
    flex: 1,
    borderRadius: theme.borderRadius.lg,
    padding: theme.spacing.xl,
    alignItems: 'center',
    justifyContent: 'center',
    ...theme.shadows.lg,
    minHeight: 140,
  },
  iconContainer: {
    width: 60,
    height: 60,
    alignItems: 'center',
    justifyContent: 'center',
    marginBottom: theme.spacing.md,
  },
  title: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize.lg,
    color: theme.colors.background,
    textAlign: 'center',
  },
  badgeContainer: {
    position: 'absolute',
    top: theme.spacing.md,
    right: theme.spacing.md,
    backgroundColor: theme.colors.star,
    borderRadius: theme.borderRadius.full,
    paddingVertical: theme.spacing.xs,
    paddingHorizontal: theme.spacing.sm,
  },
  badgeText: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize.sm,
    color: theme.colors.text,
  },
});

export default GameCard;

/**
 * Home Screen - Main dashboard
 * Shows all available games and user stats
 */

import React, { useEffect } from 'react';
import {
  View,
  ScrollView,
  StyleSheet,
  Text,
  SafeAreaView,
} from 'react-native';
import { useFocusEffect } from '@react-navigation/native';
import { theme } from '../theme';
import { useUserStore } from '../store/userStore';
import Header from '../components/Header';
import GameCard from '../components/GameCard';

interface HomeScreenProps {
  navigation: any;
}

const HomeScreen: React.FC<HomeScreenProps> = ({ navigation }) => {
  const totalStars = useUserStore((state) => state.totalStars);
  const dailyStreak = useUserStore((state) => state.dailyStreak);

  useFocusEffect(
    React.useCallback(() => {
      useUserStore.getState().updateLastPlayDate();
    }, [])
  );

  const games = [
    {
      id: 'word-puzzle',
      title: 'Word Puzzle',
      icon: '🔤',
      color: theme.colors.primary,
      screen: 'WordPuzzle',
    },
    {
      id: 'color-by-number',
      title: 'Color by Number',
      icon: '🎨',
      color: theme.colors.secondary,
      screen: 'ColorByNumber',
    },
    {
      id: 'memory-match',
      title: 'Memory Match',
      icon: '🃏',
      color: theme.colors.tertiary,
      screen: 'MemoryMatch',
    },
    {
      id: 'kids-planner',
      title: 'Kids Planner',
      icon: '📋',
      color: theme.colors.accent,
      screen: 'KidsPlanner',
    },
  ];

  return (
    <SafeAreaView style={styles.container}>
      <Header title="Tine Brain Player" stars={totalStars} />
      
      <ScrollView
        style={styles.content}
        contentContainerStyle={styles.contentContainer}
        showsVerticalScrollIndicator={false}
      >
        {/* Streak Display */}
        <View style={styles.streakCard}>
          <Text style={styles.streakLabel}>Daily Streak</Text>
          <Text style={styles.streakValue}>{dailyStreak} days 🔥</Text>
        </View>

        {/* Games Grid */}
        <View style={styles.gamesGrid}>
          {games.map((game, index) => (
            <View
              key={game.id}
              style={[
                styles.gameCardWrapper,
                { marginRight: index % 2 === 0 ? theme.spacing.md : 0 },
              ]}
            >
              <GameCard
                title={game.title}
                icon={<Text style={styles.gameIcon}>{game.icon}</Text>}
                color={game.color}
                onPress={() => navigation.navigate(game.screen)}
              />
            </View>
          ))}
        </View>

        {/* Welcome Message */}
        <Text style={styles.welcomeText}>
          Ready to play? Choose a game above! 🎮
        </Text>
      </ScrollView>
    </SafeAreaView>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: theme.colors.background,
  },
  content: {
    flex: 1,
  },
  contentContainer: {
    padding: theme.spacing.lg,
    paddingBottom: theme.spacing.xl,
  },
  streakCard: {
    backgroundColor: theme.colors.surface,
    borderRadius: theme.borderRadius.lg,
    padding: theme.spacing.lg,
    marginBottom: theme.spacing.xl,
    alignItems: 'center',
    ...theme.shadows.md,
  },
  streakLabel: {
    fontFamily: theme.typography.fontFamily.medium,
    fontSize: theme.typography.fontSize.base,
    color: theme.colors.textSecondary,
    marginBottom: theme.spacing.xs,
  },
  streakValue: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize['3xl'],
    color: theme.colors.text,
  },
  gamesGrid: {
    flexDirection: 'row',
    flexWrap: 'wrap',
    marginBottom: theme.spacing.xl,
  },
  gameCardWrapper: {
    width: '48%',
    marginBottom: theme.spacing.md,
  },
  gameIcon: {
    fontSize: 40,
  },
  welcomeText: {
    fontFamily: theme.typography.fontFamily.medium,
    fontSize: theme.typography.fontSize.base,
    color: theme.colors.textSecondary,
    textAlign: 'center',
    marginTop: theme.spacing.lg,
  },
});

export default HomeScreen;

/**
 * Word Puzzle Game Screen
 * Drag letters into correct order
 */

import React, { useState, useEffect } from 'react';
import {
  View,
  Text,
  StyleSheet,
  SafeAreaView,
  ScrollView,
  TouchableOpacity,
} from 'react-native';
import { theme } from '../theme';
import { useUserStore } from '../store/userStore';
import Header from '../components/Header';
import Button from '../components/Button';

interface WordPuzzleScreenProps {
  navigation: any;
}

const WORDS = [
  { word: 'APPLE', hint: 'A red fruit' },
  { word: 'HELLO', hint: 'A greeting' },
  { word: 'HAPPY', hint: 'Feeling joy' },
  { word: 'SMILE', hint: 'Happy face' },
  { word: 'SUNNY', hint: 'Bright day' },
];

const WordPuzzleScreen: React.FC<WordPuzzleScreenProps> = ({ navigation }) => {
  const totalStars = useUserStore((state) => state.totalStars);
  const addStars = useUserStore((state) => state.addStars);
  
  const [currentWordIndex, setCurrentWordIndex] = useState(0);
  const [guess, setGuess] = useState<string[]>([]);
  const [revealed, setRevealed] = useState(false);
  const [message, setMessage] = useState('');

  const currentWord = WORDS[currentWordIndex];
  const shuffled = currentWord.word.split('').sort(() => Math.random() - 0.5);

  const handleLetterPress = (letter: string, index: number) => {
    if (!guess.includes(letter + '_' + index)) {
      setGuess([...guess, letter + '_' + index]);
    }
  };

  const handleRemoveLetter = (index: number) => {
    setGuess(guess.filter((_, i) => i !== index));
  };

  const checkAnswer = () => {
    const guessWord = guess
      .map((item) => item.split('_')[0])
      .join('')
      .toUpperCase();
    
    if (guessWord === currentWord.word) {
      setRevealed(true);
      setMessage('🎉 Correct!');
      addStars(10);
      setTimeout(() => {
        if (currentWordIndex < WORDS.length - 1) {
          setCurrentWordIndex(currentWordIndex + 1);
          setGuess([]);
          setRevealed(false);
          setMessage('');
        } else {
          setMessage('You completed all words! 🌟');
        }
      }, 2000);
    } else {
      setMessage('Try again!');
    }
  };

  const handleSkip = () => {
    setCurrentWordIndex((currentWordIndex + 1) % WORDS.length);
    setGuess([]);
    setRevealed(false);
    setMessage('');
  };

  return (
    <SafeAreaView style={styles.container}>
      <Header title="Word Puzzle" stars={totalStars} />
      
      <ScrollView
        style={styles.content}
        contentContainerStyle={styles.contentContainer}
        showsVerticalScrollIndicator={false}
      >
        {/* Progress */}
        <Text style={styles.progress}>
          Word {currentWordIndex + 1} of {WORDS.length}
        </Text>

        {/* Hint */}
        <View style={styles.hintCard}>
          <Text style={styles.hintLabel}>Hint:</Text>
          <Text style={styles.hintText}>{currentWord.hint}</Text>
        </View>

        {/* Word Display (Blank) */}
        <View style={styles.wordDisplay}>
          {currentWord.word.split('').map((_, index) => (
            <View
              key={index}
              style={[
                styles.letterSlot,
                guess[index] && styles.letterSlotFilled,
              ]}
            >
              <Text style={styles.slotText}>
                {guess[index]?.split('_')[0] || ''}
              </Text>
            </View>
          ))}
        </View>

        {/* Guessed Letters */}
        {guess.length > 0 && (
          <View style={styles.guessedSection}>
            <Text style={styles.sectionLabel}>Your answer:</Text>
            <View style={styles.guessedLetters}>
              {guess.map((item, index) => (
                <TouchableOpacity
                  key={index}
                  style={styles.guessedLetter}
                  onPress={() => handleRemoveLetter(index)}
                >
                  <Text style={styles.guessedLetterText}>
                    {item.split('_')[0]}
                  </Text>
                </TouchableOpacity>
              ))}
            </View>
          </View>
        )}

        {/* Available Letters */}
        <View style={styles.lettersSection}>
          <Text style={styles.sectionLabel}>Tap letters to spell:</Text>
          <View style={styles.lettersGrid}>
            {shuffled.map((letter, index) => (
              <TouchableOpacity
                key={index}
                style={styles.letterButton}
                onPress={() => handleLetterPress(letter, index)}
                disabled={guess.some((item) => item === letter + '_' + index)}
              >
                <Text style={styles.letterButtonText}>{letter}</Text>
              </TouchableOpacity>
            ))}
          </View>
        </View>

        {/* Message */}
        {message && (
          <Text
            style={[
              styles.message,
              message.includes('Try') && styles.messageTry,
            ]}
          >
            {message}
          </Text>
        )}

        {/* Buttons */}
        <View style={styles.buttonsContainer}>
          <Button
            label="Check"
            onPress={checkAnswer}
            variant="primary"
            disabled={guess.length === 0}
          />
          <Button
            label="Skip"
            onPress={handleSkip}
            variant="secondary"
            style={styles.skipButton}
          />
          <Button
            label="Back"
            onPress={() => navigation.goBack()}
            variant="tertiary"
            style={styles.skipButton}
          />
        </View>
      </ScrollView>
    </SafeAreaView>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: theme.colors.background,
  },
  content: {
    flex: 1,
  },
  contentContainer: {
    padding: theme.spacing.lg,
    paddingBottom: theme.spacing.xl,
  },
  progress: {
    fontFamily: theme.typography.fontFamily.medium,
    fontSize: theme.typography.fontSize.base,
    color: theme.colors.textSecondary,
    textAlign: 'center',
    marginBottom: theme.spacing.lg,
  },
  hintCard: {
    backgroundColor: theme.colors.surface,
    borderRadius: theme.borderRadius.md,
    padding: theme.spacing.md,
    marginBottom: theme.spacing.xl,
  },
  hintLabel: {
    fontFamily: theme.typography.fontFamily.medium,
    fontSize: theme.typography.fontSize.sm,
    color: theme.colors.textSecondary,
    marginBottom: theme.spacing.xs,
  },
  hintText: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize.lg,
    color: theme.colors.text,
  },
  wordDisplay: {
    flexDirection: 'row',
    justifyContent: 'center',
    gap: theme.spacing.md,
    marginBottom: theme.spacing.xl,
    flexWrap: 'wrap',
  },
  letterSlot: {
    width: 50,
    height: 50,
    borderRadius: theme.borderRadius.md,
    borderWidth: 2,
    borderColor: theme.colors.primary,
    alignItems: 'center',
    justifyContent: 'center',
    backgroundColor: theme.colors.surface,
  },
  letterSlotFilled: {
    backgroundColor: theme.colors.primaryLight,
    borderColor: theme.colors.primaryDark,
  },
  slotText: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize.xl,
    color: theme.colors.text,
  },
  guessedSection: {
    marginBottom: theme.spacing.lg,
  },
  sectionLabel: {
    fontFamily: theme.typography.fontFamily.medium,
    fontSize: theme.typography.fontSize.base,
    color: theme.colors.textSecondary,
    marginBottom: theme.spacing.md,
  },
  guessedLetters: {
    flexDirection: 'row',
    gap: theme.spacing.sm,
    flexWrap: 'wrap',
  },
  guessedLetter: {
    width: 45,
    height: 45,
    borderRadius: theme.borderRadius.md,
    backgroundColor: theme.colors.secondary,
    alignItems: 'center',
    justifyContent: 'center',
  },
  guessedLetterText: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize.lg,
    color: theme.colors.background,
  },
  lettersSection: {
    marginBottom: theme.spacing.xl,
  },
  lettersGrid: {
    flexDirection: 'row',
    gap: theme.spacing.sm,
    flexWrap: 'wrap',
  },
  letterButton: {
    width: '19%',
    aspectRatio: 1,
    borderRadius: theme.borderRadius.md,
    backgroundColor: theme.colors.primary,
    alignItems: 'center',
    justifyContent: 'center',
    ...theme.shadows.sm,
  },
  letterButtonText: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize.lg,
    color: theme.colors.background,
  },
  message: {
    fontFamily: theme.typography.fontFamily.bold,
    fontSize: theme.typography.fontSize.xl,
    color: theme.colors.success,
    textAlign: 'center',
    marginBottom: theme.spacing.lg,
  },
  messageTry: {
    color: theme.colors.warning,
  },
  buttonsContainer: {
    gap: theme.spacing.md,
  },
  skipButton: {
    marginTop: theme.spacing.md,
  },
});

export default WordPuzzleScreen;


  "private": true
}
