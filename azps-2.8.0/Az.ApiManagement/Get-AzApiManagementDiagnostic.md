---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: 2ff4660a0e8f4929e8f79c20a8e42e0deac11f3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698115"
---
# <span data-ttu-id="93958-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="93958-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="93958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93958-102">SYNOPSIS</span></span>
<span data-ttu-id="93958-103">서비스 수준 또는 Api 수준에서 구성 된 진단에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93958-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="93958-104">진단은 Api Management 게이트웨이에서 요청/응답을 기록 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="93958-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="93958-105">구문과</span><span class="sxs-lookup"><span data-stu-id="93958-105">SYNTAX</span></span>

### <span data-ttu-id="93958-106">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="93958-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93958-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93958-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93958-108">설명은</span><span class="sxs-lookup"><span data-stu-id="93958-108">DESCRIPTION</span></span>
<span data-ttu-id="93958-109">**AzApiManagementDiagnostic** 는 지정 된 범위에서 Api management 서비스에 구성 된 진단 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93958-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="93958-110">예제의</span><span class="sxs-lookup"><span data-stu-id="93958-110">EXAMPLES</span></span>

### <span data-ttu-id="93958-111">예제 1: 테 넌 트 범위에서 구성 된 모든 진단을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93958-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
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

<span data-ttu-id="93958-112">이 명령은 Api Management 서비스에 구성 된 모든 진단을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="93958-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="93958-113">예제 2: Api 범위에서 구성 된 모든 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="93958-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
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

<span data-ttu-id="93958-114">이 명령은 Api 범위에서 구성 된 모든 진단을 가져옵니다. `echo-api`</span><span class="sxs-lookup"><span data-stu-id="93958-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="93958-115">예제 3: Id로 지정 된 API 범위 진단 가져오기</span><span class="sxs-lookup"><span data-stu-id="93958-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
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

<span data-ttu-id="93958-116">이 명령은 `applicationinsights` api에 구성 된 진단 정보를 가져옵니다 `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="93958-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="93958-117">변수</span><span class="sxs-lookup"><span data-stu-id="93958-117">PARAMETERS</span></span>

### <span data-ttu-id="93958-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="93958-118">-ApiId</span></span>
<span data-ttu-id="93958-119">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="93958-119">Identifier of existing API.</span></span>
<span data-ttu-id="93958-120">지정 된 경우 API 범위 진단을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="93958-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="93958-121">이 매개 변수는 필수 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="93958-121">This parameters is required.</span></span>

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

### <span data-ttu-id="93958-122">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="93958-122">-Context</span></span>
<span data-ttu-id="93958-123">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="93958-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="93958-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="93958-124">This parameter is required.</span></span>

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

### <span data-ttu-id="93958-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93958-125">-DefaultProfile</span></span>
<span data-ttu-id="93958-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93958-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93958-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="93958-127">-DiagnosticId</span></span>
<span data-ttu-id="93958-128">기존 진단의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="93958-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="93958-129">지정 된 경우 제품 범위 정책이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="93958-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="93958-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="93958-130">This parameters is optional.</span></span>

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

### <span data-ttu-id="93958-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93958-131">-ResourceId</span></span>
<span data-ttu-id="93958-132">진단 또는 Api 진단의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="93958-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="93958-133">지정 된 경우 식별자를 사용 하 여 진단 검색을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="93958-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="93958-134">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="93958-134">This parameter is required.</span></span>

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

### <span data-ttu-id="93958-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93958-135">CommonParameters</span></span>
<span data-ttu-id="93958-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93958-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93958-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="93958-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93958-138">입력</span><span class="sxs-lookup"><span data-stu-id="93958-138">INPUTS</span></span>

### <span data-ttu-id="93958-139">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="93958-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="93958-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="93958-140">System.String</span></span>

## <span data-ttu-id="93958-141">출력</span><span class="sxs-lookup"><span data-stu-id="93958-141">OUTPUTS</span></span>

### <span data-ttu-id="93958-142">ApiManagement. ServiceManagement. \ PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="93958-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="93958-143">상속자</span><span class="sxs-lookup"><span data-stu-id="93958-143">NOTES</span></span>

## <span data-ttu-id="93958-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93958-144">RELATED LINKS</span></span>
