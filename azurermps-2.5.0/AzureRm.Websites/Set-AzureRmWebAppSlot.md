---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 245ce5ab011f03b8d8331b5d80fa4eeb01e19e15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882414"
---
# Set-AzureRmWebAppSlot

## SYNOPSIS
Azure Web App 슬롯을 수정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### S1
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 구성원과
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Set-AzureRmWebApp** Cmdlet은 Azure 웹 앱 슬롯을 설정 합니다.

## 예제의

### 예제 1
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

이 명령은 리소스 그룹 기본값과 연결 된 웹 앱 ContosoWebApp에 해당 하는 슬롯 Slot001에 대해 HttpLoggingEnabled를 true로 설정 합니다.

## 변수

### -AppServicePlan
App Service 계획 이름

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppSettings
앱 설정 해시 테이블

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoSwapSlotName
자동 바꾸기의 대상 슬롯 이름

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionStrings
연결 문자열 해시 테이블

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultDocuments
기본 문서 문자열 배열

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
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

### -DetailedErrorLoggingEnabled
자세한 오류 로깅 사용 부울

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HandlerMappings
처리기 매핑 IList

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpLoggingEnabled
HttpLoggingEnabled 부울

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedPipelineMode
관리 되는 파이프라인 모드 이름

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
Web app 이름

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetFrameworkVersion
Net Framework 버전

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfWorkers
할당할 작업자의 수입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PhpVersion
Php 버전

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestTracingEnabled
추적을 사용 하 여 부울 요청

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -슬롯
Web app 슬롯 이름

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Use32BitWorkerProcess
32 비트 작업자 프로세스 부울 사용

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web app
Web app 개체

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebSocketsEnabled
웹 소켓 사용 부울

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -HttpsOnly
기존 슬롯에서 모든 트래픽을 HTTPS로 리디렉션하는 기능 설정/해제

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -Id 할당
기존 슬롯에서 MSI 사용/사용 안 함 [PREVIEW]

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
백그라운드에서 cmdlet 실행

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### Int32
' NumberOfWorkers ' 매개 변수는 파이프라인에서 ' Int32 ' 형식의 값을 허용 합니다.

### Site
' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.

## 출력

## 상속자

## 관련 링크

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[새로운 AzureRMWebAppSlot](./New-AzureRMWebAppSlot.md)

[제거-AzureRMWebAppSlot](./Remove-AzureRMWebAppSlot.md)

[다시 시작-AzureRMWebAppSlot](./Restart-AzureRMWebAppSlot.md)

[시작-AzureRMWebAppSlot](./Start-AzureRMWebAppSlot.md)

[중지-AzureRMWebAppSlot](./Stop-AzureRMWebAppSlot.md)

[Get-AzureRmAppServicePlan](./Get-AzureRmAppServicePlan.md)
