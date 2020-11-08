---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045448"
---
# Select-AzureStorSimpleResource

## SYNOPSIS
자원을 현재 자원으로 설정 합니다.

## 구문과

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**선택-AzureStorSimpleResource** cmdlet은 리소스를 현재 리소스로 설정 합니다.
리소스를 선택 하면 다른 cmdlet이 해당 리소스 컨텍스트 내에서 적용 됩니다.

## 예제의

### 예제 1: 처음으로 자원 선택
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

이 명령은 Contoso64-Tsqa 이라는 리소스를 현재 컨텍스트로 선택 합니다.
이 예제에서는 이전에 컴퓨터에이 컨텍스트가 초기화 되지 않았으므로 *Registrationkey* 매개 변수에 대 한 값을 지정 해야 합니다.

### 예제 2: 리소스 선택 시도
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### 예제 3: 이전에 선택한 리소스 선택
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

이 명령은 Contoso64-Tsqa 이라는 리소스를 현재 컨텍스트로 선택 합니다.
이 예제에서는 해당 컨텍스트가 이전에 선택 되어 있으므로 *Registrationkey* 매개 변수에 대 한 값을 지정할 필요가 없습니다.

## 변수

### -프로필
Azure 프로필을 지정 합니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistrationKey
등록 키를 지정 합니다.
자원을 처음 선택할 때 키를 지정 합니다.
이 cmdlet은 현재 리소스를 선택 하면 필요에 따라 cmdlet에서이 키를 사용 합니다.
자세한 내용은 Microsoft 개발자 네트워크에서 [서비스 등록 키 가져오기를](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  참조 하세요 https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context.resourcename
현재 자원으로 선택할 리소스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### StorSimpleResourceContext
이 cmdlet은 리소스 컨텍스트에 대 한 세부 정보를 포함 하는 **StorSimpleResourceContext** 개체를 반환 합니다.

## 상속자

## 관련 링크

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)


