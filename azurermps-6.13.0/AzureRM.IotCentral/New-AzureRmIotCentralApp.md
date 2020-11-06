---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/new-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
ms.openlocfilehash: d0bb10324c1a97b6228a26a7ab079edb4845d48a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537612"
---
# New-AzureRmIotCentralApp

## SYNOPSIS
새 IoT 중앙 응용 프로그램을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
제공 된 속성 및 메타 데이터로 새 IoT 중앙 응용 프로그램을 만듭니다. IoT Central 소개에 대 한 자세한 내용은을 참조 https://docs.microsoft.com/en-us/azure/iot-central/ 하세요.

## 예제의

### 예제 1 간단한 IoT 중앙 응용 프로그램을 만듭니다.
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

출력 예:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName Type: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: Sku: Microsoft. p r o. r a p. p r a p. r a p: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX 이름 DisplayName: MyAppResourceName 하위 도메인: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

표준 가격 책정 계층 S1에서 리소스 그룹의 영역에 IoT 중앙 응용 프로그램을 만듭니다.

### 예제 2 간단한 IoT 중앙 응용 프로그램을 만듭니다.
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

출력 예:

ResourceId:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. IoTCentral/Iotcentral/MyAppResourceName Name: MyAppResourceName 유형: Microsoft. IoTCentral/Iotcentral 위치: westus Tag: Sku: Microsoft Azure. p s p. p r o: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName: My 사용자 지정 표시 이름 하위 도메인: MyAppSubdomain Template: iotc-default@1.0.0 SubscriptionId: Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName

Iotc-기본 템플릿을 기반으로 하는 사용자 지정 표시 이름을 사용 하 여 ' westus ' 영역에 표준 가격 책정 계층 S1을 사용 하 여 IoT 중앙 응용 프로그램을 만듭니다.

## 변수

### -AsJob
백그라운드에서 cmdlet을 작업으로 실행 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DisplayName
IoT 중앙 응용 프로그램의 사용자 지정 표시 이름입니다.
기본값은 자원 이름입니다.

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

### -위치
IoT 중앙 응용 프로그램의 위치입니다.
기본값은 대상 리소스 그룹의 위치입니다.

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

### -이름
Iot 중앙 응용 프로그램 리소스의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

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

### -Sku
IoT 중앙 응용 프로그램에 대 한 가격 책정 계층입니다.
기본값은 S1입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -하위 도메인
IoT 중앙 URL의 하위 도메인입니다.
각 응용 프로그램에는 고유한 하위 도메인이 있어야 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
Iot 중앙 응용 프로그램 리소스 태그

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Template
IoT 중앙 응용 프로그램 서식 파일 이름입니다.
기본값은 사용자 지정 응용 프로그램입니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
### System.webserver. 컬렉션 테이블
## 출력

### PSIotCentralApp를 통해 서 .exe.
## 상속자

## 관련 링크
