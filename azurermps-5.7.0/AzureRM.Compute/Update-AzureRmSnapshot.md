---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: ff70d3879685b0cdc9fcc42732a68e6b85bbd580
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525240"
---
# Update-AzureRmSnapshot

## SYNOPSIS
스냅숏을 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### DefaultParameter (기본값)
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <SnapshotUpdate> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FriendMethod
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <Snapshot> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**업데이트 AzureRmSnapshot** cmdlet은 스냅숏을 업데이트 합니다.

## 예제의

### 예제 1
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 빈 스냅샷 업데이트 개체를 만듭니다.  또한 Windows OS 종류를 설정 하 고 암호화 설정을 사용 합니다.
두 번째 및 세 번째 명령은 스냅샷 업데이트 개체에 대 한 디스크 암호화 키 및 키 암호화 키 설정을 설정 합니다.
마지막 명령은 snapshot update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.

### 예제 2
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Snapshot01 ' 인 기존 스냅숏을 업데이트 합니다.

### 예제 3
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

또한이 명령은 리소스 그룹 ' ResourceGroup01 '에서 10gb 디스크 크기로 이름이 ' Snapshot01 ' 인 기존 스냅샷을 업데이트 합니다.

## 변수

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -스냅숏
로컬 스냅숏 개체를 지정 합니다.

```yaml
Type: Snapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SnapshotName
스냅숏의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SnapshotUpdate
로컬 스냅숏 업데이트 개체를 지정 합니다.

```yaml
Type: SnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열
SnapshotUpdate. 관리. a. i. i m a. 스냅샷

## 출력

### System. 개체

## 상속자

## 관련 링크

