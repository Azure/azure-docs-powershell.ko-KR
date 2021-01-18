---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494384"
---
# <span data-ttu-id="ac5ea-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ac5ea-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="ac5ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac5ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5ea-103">PsAzureApiManagementContext의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ac5ea-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="ac5ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac5ea-104">SYNTAX</span></span>

### <span data-ttu-id="ac5ea-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ac5ea-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac5ea-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac5ea-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac5ea-107">설명</span><span class="sxs-lookup"><span data-stu-id="ac5ea-107">DESCRIPTION</span></span>
<span data-ttu-id="ac5ea-108">**New-AzApiManagementContext** cmdlet은 **PsAzureApiManagementContext의 인스턴스를 만듭니다.**</span><span class="sxs-lookup"><span data-stu-id="ac5ea-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="ac5ea-109">컨텍스트는 모든 API Management 서비스 cmdlet에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac5ea-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="ac5ea-110">예제</span><span class="sxs-lookup"><span data-stu-id="ac5ea-110">EXAMPLES</span></span>

### <span data-ttu-id="ac5ea-111">예제 1: PsApiManagementContext 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="ac5ea-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="ac5ea-112">이 명령은 **PsApiManagementContext의 인스턴스를 만듭니다.**</span><span class="sxs-lookup"><span data-stu-id="ac5ea-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="ac5ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac5ea-113">PARAMETERS</span></span>

### <span data-ttu-id="ac5ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5ea-114">-DefaultProfile</span></span>
<span data-ttu-id="ac5ea-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac5ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac5ea-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac5ea-116">-ResourceGroupName</span></span>
<span data-ttu-id="ac5ea-117">API Management 서비스가 배포되는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac5ea-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac5ea-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac5ea-118">-ResourceId</span></span>
<span data-ttu-id="ac5ea-119">ApiManagement 서비스의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ac5ea-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="ac5ea-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ac5ea-120">This parameter is required.</span></span>

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

### <span data-ttu-id="ac5ea-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ac5ea-121">-ServiceName</span></span>
<span data-ttu-id="ac5ea-122">배포된 API Management 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac5ea-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac5ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5ea-123">CommonParameters</span></span>
<span data-ttu-id="ac5ea-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac5ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5ea-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac5ea-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5ea-126">입력</span><span class="sxs-lookup"><span data-stu-id="ac5ea-126">INPUTS</span></span>

### <span data-ttu-id="ac5ea-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ac5ea-127">System.String</span></span>

## <span data-ttu-id="ac5ea-128">출력</span><span class="sxs-lookup"><span data-stu-id="ac5ea-128">OUTPUTS</span></span>

### <span data-ttu-id="ac5ea-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ac5ea-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="ac5ea-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac5ea-130">NOTES</span></span>

## <span data-ttu-id="ac5ea-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac5ea-131">RELATED LINKS</span></span>
