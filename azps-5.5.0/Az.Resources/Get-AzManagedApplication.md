---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178825"
---
# <span data-ttu-id="f5a97-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="f5a97-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="f5a97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5a97-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a97-103">관리되는 애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-103">Gets managed applications</span></span>

## <span data-ttu-id="f5a97-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5a97-104">SYNTAX</span></span>

### <span data-ttu-id="f5a97-105">GetBySubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="f5a97-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5a97-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5a97-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5a97-107">GetById</span><span class="sxs-lookup"><span data-stu-id="f5a97-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5a97-108">설명</span><span class="sxs-lookup"><span data-stu-id="f5a97-108">DESCRIPTION</span></span>
<span data-ttu-id="f5a97-109">**Get-AzManagedApplication** cmdlet은 관리되는 애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="f5a97-110">예제</span><span class="sxs-lookup"><span data-stu-id="f5a97-110">EXAMPLES</span></span>

### <span data-ttu-id="f5a97-111">예제 1: 리소스 그룹에서 모든 관리되는 애플리케이션을 얻게</span><span class="sxs-lookup"><span data-stu-id="f5a97-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="f5a97-112">이 명령은 리소스 그룹 "MyRG"에서 관리되는 애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="f5a97-113">예제 2: 모든 관리되는 애플리케이션을 얻게</span><span class="sxs-lookup"><span data-stu-id="f5a97-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="f5a97-114">이 명령은 현재 구독에서 모든 관리되는 애플리케이션을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="f5a97-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5a97-115">PARAMETERS</span></span>

### <span data-ttu-id="f5a97-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f5a97-116">-ApiVersion</span></span>
<span data-ttu-id="f5a97-117">설정되면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f5a97-118">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a97-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a97-119">-DefaultProfile</span></span>
<span data-ttu-id="f5a97-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5a97-121">-Id</span><span class="sxs-lookup"><span data-stu-id="f5a97-121">-Id</span></span>
<span data-ttu-id="f5a97-122">구독을 포함하여 정식으로 관리되는 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="f5a97-123">예: /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f5a97-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a97-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f5a97-124">-Name</span></span>
<span data-ttu-id="f5a97-125">관리되는 애플리케이션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a97-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="f5a97-126">-Pre</span></span>
<span data-ttu-id="f5a97-127">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a97-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a97-128">-ResourceGroupName</span></span>
<span data-ttu-id="f5a97-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a97-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a97-130">CommonParameters</span></span>
<span data-ttu-id="f5a97-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a97-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a97-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5a97-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a97-133">입력</span><span class="sxs-lookup"><span data-stu-id="f5a97-133">INPUTS</span></span>

### <span data-ttu-id="f5a97-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f5a97-134">System.String</span></span>

## <span data-ttu-id="f5a97-135">출력</span><span class="sxs-lookup"><span data-stu-id="f5a97-135">OUTPUTS</span></span>

### <span data-ttu-id="f5a97-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f5a97-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f5a97-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5a97-137">NOTES</span></span>

## <span data-ttu-id="f5a97-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5a97-138">RELATED LINKS</span></span>
