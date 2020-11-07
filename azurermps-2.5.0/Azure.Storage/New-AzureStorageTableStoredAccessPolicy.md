---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 21e289ce0a8e7ca2d430d64ab9cc75bfd0c1a3ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882734"
---
# New-AzureStorageTableStoredAccessPolicy

## SYNOPSIS
Azure storage 테이블에 대 한 저장 된 액세스 정책을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureStorageTableStoredAccessPolicy** Cmdlet은 Azure storage 테이블에 대해 저장 된 액세스 정책을 만듭니다.

## 예제의

### 예제 1: 테이블에 저장 된 액세스 정책 만들기
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

이 명령은 MyTable 이라는 저장소 테이블에 Policy02 라는 액세스 정책을 만듭니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -ExpiryTime
저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -사용 권한
저장 된 액세스 정책에서 저장소 테이블에 액세스 하는 데 필요한 권한을 지정 합니다.
이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.

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

### -정책
저장 된 액세스 정책의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -테이블
Azure 저장소 테이블 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft. Azure. 일반. IStorageContext

## 출력

### System. 문자열

## 상속자

## 관련 링크

[Get-AzureStorageTableStoredAccessPolicy](./Get-AzureStorageTableStoredAccessPolicy.md)

[새로운 AzureStorageContext](./New-AzureStorageContext.md)

[제거-AzureStorageTableStoredAccessPolicy](./Remove-AzureStorageTableStoredAccessPolicy.md)

[Set-AzureStorageTableStoredAccessPolicy](./Set-AzureStorageTableStoredAccessPolicy.md)


