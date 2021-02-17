---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178820"
---
# <span data-ttu-id="1f076-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="1f076-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="1f076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f076-102">SYNOPSIS</span></span>
<span data-ttu-id="1f076-103">관리되는 애플리케이션 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-103">Gets managed application definitions</span></span>

## <span data-ttu-id="1f076-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f076-104">SYNTAX</span></span>

### <span data-ttu-id="1f076-105">GetByNameAndResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="1f076-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f076-106">GetById</span><span class="sxs-lookup"><span data-stu-id="1f076-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f076-107">설명</span><span class="sxs-lookup"><span data-stu-id="1f076-107">DESCRIPTION</span></span>
<span data-ttu-id="1f076-108">**Get-AzManagedApplicationDefinition** cmdlet은 관리되는 애플리케이션 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="1f076-109">예제</span><span class="sxs-lookup"><span data-stu-id="1f076-109">EXAMPLES</span></span>

### <span data-ttu-id="1f076-110">예제 1: 리소스 그룹에서 모든 관리되는 애플리케이션 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="1f076-111">이 명령은 리소스 그룹 "MyRG"에서 관리되는 애플리케이션 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="1f076-112">예제 2: 관리되는 애플리케이션 정의를 얻게</span><span class="sxs-lookup"><span data-stu-id="1f076-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="1f076-113">이 명령은 리소스 그룹 "MyRG"에서 관리되는 애플리케이션 정의 "myManagedAppDef"를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="1f076-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f076-114">PARAMETERS</span></span>

### <span data-ttu-id="1f076-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1f076-115">-ApiVersion</span></span>
<span data-ttu-id="1f076-116">설정되면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1f076-117">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1f076-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f076-118">-DefaultProfile</span></span>
<span data-ttu-id="1f076-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f076-120">-Id</span><span class="sxs-lookup"><span data-stu-id="1f076-120">-Id</span></span>
<span data-ttu-id="1f076-121">구독을 포함하여 정식으로 관리되는 애플리케이션 정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="1f076-122">예: /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1f076-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f076-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1f076-123">-Name</span></span>
<span data-ttu-id="1f076-124">관리되는 애플리케이션 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="1f076-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="1f076-125">-Pre</span></span>
<span data-ttu-id="1f076-126">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1f076-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f076-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f076-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-128">The resource group name.</span></span>

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

### <span data-ttu-id="1f076-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f076-129">CommonParameters</span></span>
<span data-ttu-id="1f076-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f076-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f076-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f076-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f076-132">입력</span><span class="sxs-lookup"><span data-stu-id="1f076-132">INPUTS</span></span>

### <span data-ttu-id="1f076-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1f076-133">System.String</span></span>

## <span data-ttu-id="1f076-134">출력</span><span class="sxs-lookup"><span data-stu-id="1f076-134">OUTPUTS</span></span>

### <span data-ttu-id="1f076-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="1f076-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1f076-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f076-136">NOTES</span></span>

## <span data-ttu-id="1f076-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f076-137">RELATED LINKS</span></span>
