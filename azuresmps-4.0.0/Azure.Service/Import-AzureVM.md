---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7180CAC6-BFC1-4A18-A754-83D5F05C5BEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: c62c30558147bccd9cdecc73925b7e1a379d1c5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046255"
---
# Import-AzureVM

## SYNOPSIS
파일에서 Azure 가상 컴퓨터 상태를 가져옵니다.

## 구문과

```
Import-AzureVM [-Path] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
**가져오기-add-azurevm** cmdlet은 이전에 저장 된 가상 컴퓨터의 상태를 XML 파일에서 가져옵니다.
이 cmdlet은 가져온 데이터에서 가상 컴퓨터를 만들 때 유용 합니다.

**Export-** a 2를 실행 하 고 **제거한** 후에는 **-** add-azurevm를 가져와 가상 컴퓨터를 다시 만들면 결과 가상 컴퓨터의 IP 주소가 원본과 다를 수 있습니다.

## 예제의

### 예제 1: 가상 컴퓨터 상태 가져오기
```
PS C:\> Import-AzureVM -Path "C:\VMstate.xml" | New-AzureVM -ServiceName "ContosoService02"
```

이 명령은 VMstate.xml 파일에서 가상 컴퓨터의 상태를 가져온 다음 지정 된 클라우드 서비스에서 가상 컴퓨터를 만듭니다.

## 변수

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
이전에 저장 된 가상 컴퓨터 상태를 사용 하 여 파일의 경로를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[수출-Add-azurevm](./Export-AzureVM.md)

[뉴욕](./New-AzureVM.md)


