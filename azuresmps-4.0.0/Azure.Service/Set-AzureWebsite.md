---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045433"
---
# <span data-ttu-id="0ba4f-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0ba4f-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="0ba4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ba4f-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba4f-103">Azure에서 실행 되는 웹 사이트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="0ba4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ba4f-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ba4f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ba4f-105">DESCRIPTION</span></span>
<span data-ttu-id="0ba4f-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0ba4f-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0ba4f-108">**AzureWebsite** Cmdlet은 Azure에서 실행 되는 웹 사이트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="0ba4f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0ba4f-109">EXAMPLES</span></span>

### <span data-ttu-id="0ba4f-110">예제 1: 웹 사이트에 대해 HTTP 로깅 사용</span><span class="sxs-lookup"><span data-stu-id="0ba4f-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="0ba4f-111">이 예제에서는 HTTP 로깅을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="0ba4f-112">예제 2: 웹 사이트의 저장소 자격 증명 설정</span><span class="sxs-lookup"><span data-stu-id="0ba4f-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="0ba4f-113">이 예제에서는 AZURE_STORAGE_ACCOUNT 및 AZURE_STORAGE_ACCESS_KEY에 대 한 환경 변수를 사용 하 여 myWebsite 이라는 웹 사이트의 저장소 자격 증명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="0ba4f-114">변수</span><span class="sxs-lookup"><span data-stu-id="0ba4f-114">PARAMETERS</span></span>

### <span data-ttu-id="0ba4f-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="0ba4f-115">-AppSettings</span></span>
<span data-ttu-id="0ba4f-116">웹 사이트에 사용 되는 환경 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-116">Specifies the environment variables that will be used by the website.</span></span>

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

### <span data-ttu-id="0ba4f-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="0ba4f-117">-AutoSwapSlotName</span></span>
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

### <span data-ttu-id="0ba4f-118">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="0ba4f-118">-ConnectionStrings</span></span>
<span data-ttu-id="0ba4f-119">웹 사이트에 사용 되는 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-120">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="0ba4f-120">-DefaultDocuments</span></span>
<span data-ttu-id="0ba4f-121">웹 사이트를 검색할 때 자동으로 표시 되는 문서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ba4f-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="0ba4f-123">웹 사이트에 대 한 자세한 IIS 오류가 기록 되는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="0ba4f-124">-HandlerMappings</span></span>
<span data-ttu-id="0ba4f-125">웹 사이트에서 사용 하는 처리기 매핑을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-126">-호스트 이름</span><span class="sxs-lookup"><span data-stu-id="0ba4f-126">-HostNames</span></span>
<span data-ttu-id="0ba4f-127">웹 사이트에 액세스 하는 데 사용할 수 있는 정규화 된 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ba4f-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="0ba4f-129">웹 사이트에 대해 http 로깅을 사용할지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="0ba4f-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="0ba4f-131">관리 되는 파이프라인 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0ba4f-132">-Metadata</span></span>
<span data-ttu-id="0ba4f-133">웹 사이트에 대 한 메타 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-134">-이름</span><span class="sxs-lookup"><span data-stu-id="0ba4f-134">-Name</span></span>
<span data-ttu-id="0ba4f-135">웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-135">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="0ba4f-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="0ba4f-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="0ba4f-137">웹 사이트에 필요한 .Net Framework 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-137">Specifies the version of the .Net Framework required by the website.</span></span>

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

### <span data-ttu-id="0ba4f-138">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="0ba4f-138">-NumberOfWorkers</span></span>
<span data-ttu-id="0ba4f-139">웹 사이트를 실행 하는 작업자 프로세스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ba4f-140">-PassThru</span></span>
<span data-ttu-id="0ba4f-141">이 cmdlet이 **부울** 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

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

### <span data-ttu-id="0ba4f-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="0ba4f-142">-PhpVersion</span></span>
<span data-ttu-id="0ba4f-143">웹 사이트에 필요한 PHP 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-143">Specifies the PHP version required by the website.</span></span>

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

### <span data-ttu-id="0ba4f-144">-프로필</span><span class="sxs-lookup"><span data-stu-id="0ba4f-144">-Profile</span></span>
<span data-ttu-id="0ba4f-145">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ba4f-146">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0ba4f-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ba4f-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="0ba4f-148">웹 사이트에 대 한 요청 추적이 사용 되는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="0ba4f-149">-RoutingRules</span></span>
<span data-ttu-id="0ba4f-150">프로덕션에서 테스트 하는 데 사용할 라우팅 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="0ba4f-151">-SiteWithConfig</span></span>
<span data-ttu-id="0ba4f-152">웹 사이트에 사용 되는 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-153">-슬롯</span><span class="sxs-lookup"><span data-stu-id="0ba4f-153">-Slot</span></span>
<span data-ttu-id="0ba4f-154">웹 사이트의 슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-154">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="0ba4f-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="0ba4f-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="0ba4f-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="0ba4f-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="0ba4f-158">32 비트 모드를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="0ba4f-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="0ba4f-160">Websocket을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ba4f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba4f-161">CommonParameters</span></span>
<span data-ttu-id="0ba4f-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba4f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba4f-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ba4f-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba4f-164">입력</span><span class="sxs-lookup"><span data-stu-id="0ba4f-164">INPUTS</span></span>

## <span data-ttu-id="0ba4f-165">출력</span><span class="sxs-lookup"><span data-stu-id="0ba4f-165">OUTPUTS</span></span>

## <span data-ttu-id="0ba4f-166">상속자</span><span class="sxs-lookup"><span data-stu-id="0ba4f-166">NOTES</span></span>

## <span data-ttu-id="0ba4f-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ba4f-167">RELATED LINKS</span></span>

[<span data-ttu-id="0ba4f-168">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0ba4f-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="0ba4f-169">새로운 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0ba4f-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="0ba4f-170">제거-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0ba4f-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


