---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525959"
---
# Get-AzureRmStorageContainer

## SYNOPSIS
저장소 blob 컨테이너를 가져오거나 나열 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### AccountName (기본값)
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AccountObject
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Get-AzureRmStorageContainer** Cmdlet은 저장소 blob 컨테이너를 가져오거나 나열 합니다.

## 예제의

### 예제 1: 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너 가져오기
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

이 명령은 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너를 가져옵니다.

### 예제 2: 저장소 계정의 모든 저장소 blob 컨테이너 나열
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

이 명령은 저장소 계정 이름이 있는 저장소 계정의 모든 저장소 blob 컨테이너를 나열 합니다.

### 예제 3: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너를 가져옵니다.
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너를 가져옵니다.

## 변수

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
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. m a. 모델. PSContainer

## 상속자

## 관련 링크

