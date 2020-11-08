---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042243"
---
# <span data-ttu-id="3f951-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3f951-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="3f951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f951-102">SYNOPSIS</span></span>
<span data-ttu-id="3f951-103">PsAzureApiManagementContext의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="3f951-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f951-104">SYNTAX</span></span>

### <span data-ttu-id="3f951-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f951-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f951-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f951-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f951-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3f951-107">DESCRIPTION</span></span>
<span data-ttu-id="3f951-108">**AzApiManagementContext** Cmdlet은 **PsAzureApiManagementContext** 의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="3f951-109">컨텍스트는 모든 API Management 서비스 cmdlet에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="3f951-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3f951-110">EXAMPLES</span></span>

### <span data-ttu-id="3f951-111">예제 1: PsApiManagementContext 인스턴스 만들기</span><span class="sxs-lookup"><span data-stu-id="3f951-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="3f951-112">이 명령은 **PsApiManagementContext** 의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="3f951-113">변수</span><span class="sxs-lookup"><span data-stu-id="3f951-113">PARAMETERS</span></span>

### <span data-ttu-id="3f951-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f951-114">-DefaultProfile</span></span>
<span data-ttu-id="3f951-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f951-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f951-116">-ResourceGroupName</span></span>
<span data-ttu-id="3f951-117">API Management 서비스를 배포 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="3f951-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f951-118">-ResourceId</span></span>
<span data-ttu-id="3f951-119">ApiManagement 서비스의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="3f951-120">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-120">This parameter is required.</span></span>

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

### <span data-ttu-id="3f951-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3f951-121">-ServiceName</span></span>
<span data-ttu-id="3f951-122">배포 된 API Management 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-122">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="3f951-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f951-123">CommonParameters</span></span>
<span data-ttu-id="3f951-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f951-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f951-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3f951-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f951-126">입력</span><span class="sxs-lookup"><span data-stu-id="3f951-126">INPUTS</span></span>

### <span data-ttu-id="3f951-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3f951-127">System.String</span></span>

## <span data-ttu-id="3f951-128">출력</span><span class="sxs-lookup"><span data-stu-id="3f951-128">OUTPUTS</span></span>

### <span data-ttu-id="3f951-129">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3f951-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3f951-130">상속자</span><span class="sxs-lookup"><span data-stu-id="3f951-130">NOTES</span></span>

## <span data-ttu-id="3f951-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f951-131">RELATED LINKS</span></span>
