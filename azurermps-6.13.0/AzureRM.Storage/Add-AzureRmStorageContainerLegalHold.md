---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525964"
---
# Add-AzureRmStorageContainerLegalHold

## SYNOPSIS
저장소 blob 컨테이너에 legal 보존 태그 추가

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### AccountName (기본값)
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AccountObject
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContainerObject
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**Add-AzureRmStorageContainerLegalHold** Cmdlet은 저장소 blob 컨테이너에 legal 보존 태그를 추가 합니다.

## 예제의

### 예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너에 legal 보류 태그 추가
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

이 명령은 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너에 legal 보존 태그를 추가 합니다.

### 예제 2: 저장소 계정 개체 및 컨테이너 이름이 있는 저장소 blob 컨테이너에 legal 보류 태그 추가
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

이 명령은 저장소 계정 개체와 컨테이너 이름을 가진 저장소 blob 컨테이너에 legal 보존 태그를 추가 합니다.

### 예제 3: 파이프라인을 사용 하 여 저장소 계정의 모든 저장소 blob 컨테이너에 legal 보류 태그 추가
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

이 명령은 파이프라인을 사용 하 여 저장소 계정의 모든 저장소 blob 컨테이너에 legal 보존 태그를 추가 합니다.

## 변수

### -컨테이너
저장소 컨테이너 개체

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
컨테이너 이름

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccount
저장소 계정 개체

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
저장소 계정 이름입니다.

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
컨테이너 LegalHold 태그

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

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

## 출력

### PSLegalHold를 통해 관리 합니다.

## 상속자

## 관련 링크

