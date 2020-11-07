---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: c1ddf2ec1e83a73d130f5be5eee38bfc8cac4c9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698039"
---
# <span data-ttu-id="7ef10-101">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7ef10-101">New-AzApiManagementLogger</span></span>

## <span data-ttu-id="7ef10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ef10-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef10-103">API Management로 거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-103">Creates an API Management Logger.</span></span>

## <span data-ttu-id="7ef10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ef10-104">SYNTAX</span></span>

### <span data-ttu-id="7ef10-105">EventHubLoggerSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7ef10-105">EventHubLoggerSet (Default)</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ef10-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="7ef10-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ef10-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7ef10-107">DESCRIPTION</span></span>
<span data-ttu-id="7ef10-108">**AzApiManagementLogger** Cmdlet은 Azure API Management **로 거** 를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-108">The **New-AzApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="7ef10-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7ef10-109">EXAMPLES</span></span>

### <span data-ttu-id="7ef10-110">예제 1:로 거 만들기</span><span class="sxs-lookup"><span data-stu-id="7ef10-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="7ef10-111">이 명령은 지정 된 연결 문자열을 사용 하 여 ContosoSdkEventHub 이라는로 거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="7ef10-112">변수</span><span class="sxs-lookup"><span data-stu-id="7ef10-112">PARAMETERS</span></span>

### <span data-ttu-id="7ef10-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="7ef10-113">-ConnectionString</span></span>
<span data-ttu-id="7ef10-114">다음으로 시작 하는 Azure 이벤트 허브 연결 문자열을 지정 합니다. `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="7ef10-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="7ef10-115">연결 문자열에서 전송 권한이 있는 키를 구성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef10-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7ef10-116">-Context</span></span>
<span data-ttu-id="7ef10-117">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef10-118">-DefaultProfile</span></span>
<span data-ttu-id="7ef10-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ef10-120">-설명</span><span class="sxs-lookup"><span data-stu-id="7ef10-120">-Description</span></span>
<span data-ttu-id="7ef10-121">설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-121">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef10-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="7ef10-122">-InstrumentationKey</span></span>
<span data-ttu-id="7ef10-123">Application Insights의 계측 키입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="7ef10-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef10-125">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="7ef10-125">-IsBuffered</span></span>
<span data-ttu-id="7ef10-126">게시 하기 전에로 거의 레코드를 버퍼링 할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="7ef10-127">기본값은 $True입니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-127">The default value is $True.</span></span>
<span data-ttu-id="7ef10-128">레코드가 버퍼링 되 면 15 초 마다 이벤트 허브에 또는 버퍼가 256 KB의 메시지를 받을 때마다 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef10-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="7ef10-129">-LoggerId</span></span>
<span data-ttu-id="7ef10-130">로 거에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="7ef10-131">ID를 지정 하지 않으면이 cmdlet이 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-131">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef10-132">-이름</span><span class="sxs-lookup"><span data-stu-id="7ef10-132">-Name</span></span>
<span data-ttu-id="7ef10-133">Azure 클래식 포털에서 이벤트 허브의 엔터티 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef10-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef10-134">CommonParameters</span></span>
<span data-ttu-id="7ef10-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ef10-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef10-136">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ef10-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef10-137">입력</span><span class="sxs-lookup"><span data-stu-id="7ef10-137">INPUTS</span></span>

### <span data-ttu-id="7ef10-138">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7ef10-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7ef10-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7ef10-139">System.String</span></span>

### <span data-ttu-id="7ef10-140">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7ef10-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7ef10-141">출력</span><span class="sxs-lookup"><span data-stu-id="7ef10-141">OUTPUTS</span></span>

### <span data-ttu-id="7ef10-142">ApiManagement. ServiceManagement. \ PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7ef10-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="7ef10-143">상속자</span><span class="sxs-lookup"><span data-stu-id="7ef10-143">NOTES</span></span>

## <span data-ttu-id="7ef10-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ef10-144">RELATED LINKS</span></span>

[<span data-ttu-id="7ef10-145">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7ef10-145">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="7ef10-146">제거-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7ef10-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="7ef10-147">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="7ef10-147">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


