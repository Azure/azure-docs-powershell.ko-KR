---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205821"
---
# <span data-ttu-id="8b142-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8b142-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="8b142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b142-102">SYNOPSIS</span></span>
<span data-ttu-id="8b142-103">백end의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="8b142-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b142-104">SYNTAX</span></span>

### <span data-ttu-id="8b142-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8b142-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b142-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b142-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b142-107">설명</span><span class="sxs-lookup"><span data-stu-id="8b142-107">DESCRIPTION</span></span>
<span data-ttu-id="8b142-108">백end의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="8b142-109">예제</span><span class="sxs-lookup"><span data-stu-id="8b142-109">EXAMPLES</span></span>

### <span data-ttu-id="8b142-110">예제 1: 모든 백end를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="8b142-111">Api Management 서비스에 구성된 모든 백end의 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="8b142-112">예제 2: 식별자 123에서 지정한 백end를 얻게</span><span class="sxs-lookup"><span data-stu-id="8b142-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="8b142-113">식별자 '123'으로 식별된 지정된 백end의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="8b142-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b142-114">PARAMETERS</span></span>

### <span data-ttu-id="8b142-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="8b142-115">-BackendId</span></span>
<span data-ttu-id="8b142-116">백end의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-116">Identifier of a backend.</span></span>
<span data-ttu-id="8b142-117">지정된 경우 식별자에 의해 백end를 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="8b142-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="8b142-119">-Context</span><span class="sxs-lookup"><span data-stu-id="8b142-119">-Context</span></span>
<span data-ttu-id="8b142-120">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8b142-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b142-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b142-122">-DefaultProfile</span></span>
<span data-ttu-id="8b142-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b142-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b142-124">-ResourceId</span></span>
<span data-ttu-id="8b142-125">백end의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="8b142-126">지정된 경우 식별자에 의해 백end를 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="8b142-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-127">This parameter is required.</span></span>

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

### <span data-ttu-id="8b142-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b142-128">CommonParameters</span></span>
<span data-ttu-id="8b142-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b142-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b142-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b142-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b142-131">입력</span><span class="sxs-lookup"><span data-stu-id="8b142-131">INPUTS</span></span>

### <span data-ttu-id="8b142-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8b142-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8b142-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8b142-133">System.String</span></span>

## <span data-ttu-id="8b142-134">출력</span><span class="sxs-lookup"><span data-stu-id="8b142-134">OUTPUTS</span></span>

### <span data-ttu-id="8b142-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8b142-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="8b142-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b142-136">NOTES</span></span>

## <span data-ttu-id="8b142-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b142-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b142-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8b142-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="8b142-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8b142-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="8b142-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8b142-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="8b142-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8b142-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="8b142-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8b142-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
