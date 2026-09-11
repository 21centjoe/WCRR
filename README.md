# WCRR
WCRR is an advanced client-side cryptographic vault and topological self-healing data protection library developed by Joseph La Follette under AGPL-3.0. It integrates browser-native AES-256-GCM authentication, real gzip compression, and a C60 fullerene face-parity error-correction matrix to ensure resilient data preservation.

Core Architecture

Cryptographic Rigor: Utilizes the Web Crypto API (crypto.subtle) with PBKDF2 (250,000 iterations, SHA-256) for secure key derivation. Passphrases are strictly mandatory with zero default fallbacks.

C60 Fullerene Self-Healing: Generates a truncated icosahedron graph featuring 60 vertices, 90 edges, and 32 faces. Computes XOR face-parities over ciphertext chunks to isolate errors and automatically reconstruct damaged blocks prior to decryption.

Ciphertext-First Pipeline: Encrypts raw payloads before chunking and parity calculations to protect AES-256-GCM authentication boundaries during self-healing routines.

USB Workspace Minting: Leverages the File System Access API to generate air-gapped, sandboxed workspaces directly onto inserted removable drives, supporting encrypted vaults, unencrypted geometric maps, and polyglot PNG containers.

Fleet Operations: Integrates local node management for telemetry and job packet transmission.

Technical SpecificationsComponentImplementationParametersEncryptionAES-256-GCM12-byte IV, 16-byte SaltKey DerivationPBKDF2-HMAC-SHA256250,000 IterationsError CorrectionC60 Fullerene Face-Parity32 Faces, XOR ShardingCompressionCompressionStreamNative gzipSystem CoreReference ID252

API Quick Reference

wcrrEncode(fileBytes, filename, password, useGzip): Compresses, encrypts, chunks, and binds the fullerene parity matrix into a standalone binary buffer.

wcrrDecode(rawBytes, password): Parses vault headers, verifies CRCs, executes iterative parity reconstruction for damaged blocks, and decrypts payloads.

mintUSBWorkspace(): Deploys a sandboxed runner and selected payload formats to target directory handles.

License
Distributed under the AGPL-3.0 license. Copyright © 2026 Joseph La Follette, All Rights Reserved.
