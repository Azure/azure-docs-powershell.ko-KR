---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: fe1e1075e14e3752024edff1b68db88419d5bcd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531204"
---
# Register-AzureRmBackupContainer

## SYNOPSIS
백업 자격 증명 모음을 사용 하 여 컨테이너를 등록 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### V1VM
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### V2VM
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmBackupContainer** Cmdlet은 Azure Backup 자격 증명 모음을 사용 하 여 컨테이너를 등록 합니다.
Azure 백업을 사용 하 여 백업을 구성 하려면 먼저 백업 자격 증명 모음에 서버 또는 가상 컴퓨터를 등록 합니다.
이 cmdlet은 지정 된 자격 증명 모음을 사용 하 여 인프라를 서비스 (IaaS) 가상 컴퓨터로 등록 합니다.
Register 작업은 Azure 가상 컴퓨터를 백업 자격 증명 모음과 연결 하 고 백업 수명 주기를 통해 가상 컴퓨터를 추적 합니다.

## 예제의

### 예제 1: 백업 자격 증명 모음에 가상 컴퓨터 등록
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

첫 번째 명령은 Get-AzureRmBackupVault cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.
명령이 $Vault 변수에 자격 증명 모음을 저장 합니다.

두 번째 명령은 Contoso03Vm 이라는 가상 컴퓨터를 $Vault의 자격 증명 모음으로 등록 합니다.
해당 가상 머신이 ContosoService27 이라는 서비스에 속해 있습니다.

## 변수

### -이름
이 cmdlet이 등록 하는 가상 컴퓨터의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 컴퓨터에 대 한 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
이 cmdlet이 등록 하는 가상 컴퓨터의 서비스 이름을 지정 합니다.

일반적으로 클라우드 서비스 이름의 접미사는 cloudapp.net입니다.
이 매개 변수를 지정할 때는 접미사를 포함 하지 마세요.

가상 컴퓨터에 대 한 정보를 얻으려면 Get-AzureRMVM cmdlet을 사용 합니다.
서비스 이름은 가상 컴퓨터 개체의 **Deploymentname** 속성입니다.

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -저장실
이 cmdlet이 가상 컴퓨터를 등록 하는 백업 자격 증명 모음을 지정 합니다.
**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.

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

### AzureRmBackupVault

## 출력

### AzureRmBackupJob

## 상속자

## 관련 링크

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


