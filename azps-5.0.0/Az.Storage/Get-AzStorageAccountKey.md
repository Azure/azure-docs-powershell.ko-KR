---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226480"
---
# Get-AzStorageAccountKey

## SYNOPSIS
Azure 저장소 계정의 선택 키를 가져옵니다.

## 구문과

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzStorageAccountKey** Cmdlet은 Azure 저장소 계정의 선택 키를 가져옵니다.

## 예제의

### 예제 1: 저장소 계정의 선택 키 가져오기
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

이 명령은 지정 된 Azure 저장소 계정에 대 한 키를 가져옵니다.

### 예제 2: 저장소 계정에 대 한 특정 선택 키 가져오기
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### 예제 3: 저장소 계정의 선택 키 목록, Kerberos 키 포함 (active directory를 사용 하는 경우)
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

이 명령은 지정 된 Azure 저장소 계정에 대 한 키를 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListKerbKey
지정 된 저장소 계정에 대 한 Kerberos 키 (active directory를 사용할 수 있는 경우)를 나열 합니다.
Azure 파일 id 기반 인증에 대 한 저장소 계정 당 Kerberos 키가 생성 됩니다 (azure AD DS (active Directory 도메인 서비스) 또는 AD DS (Active Directory 도메인 서비스). 저장소 계정을 나타내는 도메인 서비스에 등록 된 id의 암호로 사용 됩니다. Kerberos 키는 저장소 계정에 대 한 모든 컨트롤 또는 데이터 평면 읽기 또는 쓰기 작업을 수행할 수 있는 액세스 권한을 제공 하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet에서 키를 가져오는 저장소 계정의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### StorageAccountKey를 통해 저장 합니다.

## 상속자

## 관련 링크

[새로운 AzStorageAccountKey](./New-AzStorageAccountKey.md)


