---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: c7bcddca0cfef631f7501dfb6c017f2c6ef7af25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702233"
---
# Get-AzureRmBackupContainer

## SYNOPSIS
백업 컨테이너를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Get-AzureRmBackupContainer** Cmdlet은 Azure 백업 컨테이너를 가져옵니다.

**Azurebackupcontainer** 는 데이터 원본, 보호 된 항목 및 복구 지점을 캡슐화 합니다.
**Azurebackupcontainer** 는 다음 중 하나가 될 수 있습니다. 

- Windows Server 컴퓨터
- SCDPM (System Center Data Protection Manager) 서버 
- Azure의 IaaS (서비스 인프라) 가상 컴퓨터

백업이 데이터 원본 또는 항목을 백업할 수 있으려면 먼저 Azure Backup service를 사용 하 여 저장 된 컨테이너를 등록 해야 합니다.
백업 자격 증명 모음에 백업 데이터를 보내려면 컨테이너를 인증 해야 합니다.
Windows Server 컴퓨터 및 SCDPM 서버의 경우 등록은 서버의 정규화 된 도메인 이름과 함께 유지 됩니다.

## 예제의

### 예제 1: 자격 증명 모음에 등록 된 모든 서버 보기
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

첫 번째 명령은 **AzureRmBackupVault** cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.
명령이 $Vault 변수에 해당 개체를 저장 합니다.

두 번째 명령은 $Vault의 자격 증명 모음에서 Windows 형식의 모든 컨테이너를 가져옵니다.

### 예제 2: 특정 컨테이너 가져오기
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

이 명령은 DPMSERVER 이라는 컨테이너를 가져옵니다. CONTOSO.COM.
명령은 $Vault 및 컨테이너 유형의 자격 증명 모음을 지정 합니다.

### 예제 3: 등록 된 모든 Azure 가상 컴퓨터 보기
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

이 명령은 $Vault의 자격 증명 모음에서 등록 된 가상 컴퓨터를 가져옵니다.

## 변수

### -ManagedResourceGroupName
컨테이너와 연결 된 리소스 그룹의 이름을 지정 합니다.
이 이름은 Register-AzureRmBackupContainer cmdlet의 *ServiceName* 또는 *ResourceGroupName* 매개 변수에 대해 지정한 값과 동일 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 가져오는 컨테이너의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -상태
이 cmdlet이 가져오는 컨테이너의 현재 상태를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- NotRegistered 됨 
- 되어 
- 등록

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
이 cmdlet이 가져오는 컨테이너의 유형을 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -저장실
이 cmdlet이 컨테이너를 가져오는 백업 자격 증명 모음을 지정 합니다.
**AzureRmBackupVault** 을 얻으려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### AzureBackupVault

## 출력

### AzureBackupContainer

## 상속자
* 않아야

## 관련 링크

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)

[등록 취소-AzureRmBackupContainer](./Unregister-AzureRmBackupContainer.md)


