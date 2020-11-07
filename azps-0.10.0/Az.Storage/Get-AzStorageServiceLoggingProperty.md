---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: fc1cbddd59d52816b0f7ef3bd664405a98ead518
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876293"
---
# Get-AzStorageServiceLoggingProperty

## SYNOPSIS
Azure Storage 서비스에 대 한 로깅 속성을 가져옵니다.

## 구문과

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzStorageServiceLoggingProperty** Cmdlet은 Azure 저장소 서비스에 대 한 로깅 속성을 가져옵니다.

## 예제의

### 예제 1: Blob 서비스에 대 한 로깅 속성 가져오기
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

이 명령은 blob 저장소에 대 한 로깅 속성을 가져옵니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.

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

### -ServiceType
저장소 서비스 유형을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 서비스 형식에 대 한 로깅 속성을 가져옵니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 블 
- 테이블로
- 전담팀
- 파일 값이 현재 지원 되지 않습니다.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Microsoft. Azure. 일반. IStorageContext

## 출력

### LoggingProperties/. m a w.

## 상속자

## 관련 링크

[새로운 AzStorageContext](./New-AzStorageContext.md)

[Set-AzStorageServiceLoggingProperty](./Set-AzStorageServiceLoggingProperty.md)


