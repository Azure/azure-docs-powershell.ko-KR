---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 41c1324c3762d0b6e04c0c532976c62c0a16067e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525144"
---
# Remove-AzureRmDataLakeStoreItemAclEntry

## SYNOPSIS
Data Lake Store의 파일 또는 폴더의 ACL에서 항목을 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### Removebyac(기본값)
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveSpecificACE
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmDataLakeStoreItemAclEntry** Cmdlet은 Data Lake store에 있는 파일 또는 폴더의 ACL (액세스 제어 목록)에서 항목 (ACE)을 제거 합니다.

## 예제의

### 예제 1: 사용자 항목 제거
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

이 명령은 ContosoADL 계정에서 Patti의 사용자 ACE를 제거 합니다.

## 변수

### -계정
Data Lake Store 계정의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AceType
제거할 ACE 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 클릭할
- 그룹과
- 마스킹하
- 나머지

```yaml
Type: AceType
Parameter Sets: RemoveSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Acl
제거할 항목이 포함 된 ACL 개체를 지정 합니다.

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -기본
이 작업을 수행 하면 지정 된 ACL에서 기본 ACE가 제거 됨을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Id
ACE를 제거할 AzureActive Directory 사용자, 그룹 또는 서비스 주체의 개체 ID를 지정 합니다.

```yaml
Type: Guid
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
ACE를 제거할 항목의 Data Lake Store 경로를 루트 디렉터리 (/)로 시작 하 여 지정 합니다.

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### DataLakeStoreItemAce[]
' Acl ' 매개 변수는 파이프라인에서 ' DataLakeStoreItemAce [] ' 형식의 값을 허용 합니다.

## 출력

### 부울
PassThru가 지정 된 경우 성공적으로 완료 되 면 true를 반환 합니다.

## 상속자

## 관련 링크

[Set-AzureRmDataLakeStoreItemAclEntry](./Set-AzureRmDataLakeStoreItemAclEntry.md)


