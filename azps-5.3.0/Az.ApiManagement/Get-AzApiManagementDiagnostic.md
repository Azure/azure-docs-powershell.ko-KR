---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: c31c3d23e8e5ed160aff55a3599137454f1c638c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494466"
---
# <span data-ttu-id="5862a-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5862a-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="5862a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5862a-102">SYNOPSIS</span></span>
<span data-ttu-id="5862a-103">서비스 수준 또는 API 수준에서 구성된 진단에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="5862a-104">진단은 Api Management 게이트웨이에서 요청/응답을 기록하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="5862a-105">구문</span><span class="sxs-lookup"><span data-stu-id="5862a-105">SYNTAX</span></span>

### <span data-ttu-id="5862a-106">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5862a-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5862a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5862a-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5862a-108">설명</span><span class="sxs-lookup"><span data-stu-id="5862a-108">DESCRIPTION</span></span>
<span data-ttu-id="5862a-109">**Get-AzApiManagementDiagnostic은** 주어진 범위에서 API 관리 서비스에 구성된 진단의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="5862a-110">예제</span><span class="sxs-lookup"><span data-stu-id="5862a-110">EXAMPLES</span></span>

### <span data-ttu-id="5862a-111">예제 1: 테넌트 범위에서 구성된 모든 진단을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="5862a-112">이 명령은 Api Management 서비스에 구성된 모든 진단을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="5862a-113">예제 2: API 범위에서 구성된 모든 진단을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="5862a-114">이 명령은 API 범위에 구성된 모든 `echo-api` 진단을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="5862a-115">예제 3: ID로 지정된 API 범위 진단을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="5862a-116">이 명령은 `applicationinsights` API에 구성된 진단을 `echo-api` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="5862a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5862a-117">PARAMETERS</span></span>

### <span data-ttu-id="5862a-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5862a-118">-ApiId</span></span>
<span data-ttu-id="5862a-119">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-119">Identifier of existing API.</span></span>
<span data-ttu-id="5862a-120">지정된 경우 API 범위 진단을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="5862a-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-121">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5862a-122">-Context</span><span class="sxs-lookup"><span data-stu-id="5862a-122">-Context</span></span>
<span data-ttu-id="5862a-123">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5862a-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5862a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5862a-125">-DefaultProfile</span></span>
<span data-ttu-id="5862a-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5862a-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="5862a-127">-DiagnosticId</span></span>
<span data-ttu-id="5862a-128">기존 진단의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="5862a-129">지정된 경우 제품 범위 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="5862a-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-130">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5862a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5862a-131">-ResourceId</span></span>
<span data-ttu-id="5862a-132">진단 또는 Api 진단의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="5862a-133">지정된 경우 식별자에 의해 진단을 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="5862a-134">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5862a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5862a-135">CommonParameters</span></span>
<span data-ttu-id="5862a-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5862a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5862a-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5862a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5862a-138">입력</span><span class="sxs-lookup"><span data-stu-id="5862a-138">INPUTS</span></span>

### <span data-ttu-id="5862a-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5862a-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5862a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5862a-140">System.String</span></span>

## <span data-ttu-id="5862a-141">출력</span><span class="sxs-lookup"><span data-stu-id="5862a-141">OUTPUTS</span></span>

### <span data-ttu-id="5862a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5862a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="5862a-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5862a-143">NOTES</span></span>

## <span data-ttu-id="5862a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5862a-144">RELATED LINKS</span></span>
