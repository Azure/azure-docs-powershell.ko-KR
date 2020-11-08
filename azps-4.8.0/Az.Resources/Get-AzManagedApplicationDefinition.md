---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212695"
---
# <span data-ttu-id="964bd-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="964bd-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="964bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="964bd-102">SYNOPSIS</span></span>
<span data-ttu-id="964bd-103">관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-103">Gets managed application definitions</span></span>

## <span data-ttu-id="964bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="964bd-104">SYNTAX</span></span>

### <span data-ttu-id="964bd-105">GetByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="964bd-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="964bd-106">GetById</span><span class="sxs-lookup"><span data-stu-id="964bd-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="964bd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="964bd-107">DESCRIPTION</span></span>
<span data-ttu-id="964bd-108">**Get-AzManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="964bd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="964bd-109">EXAMPLES</span></span>

### <span data-ttu-id="964bd-110">예제 1: 리소스 그룹에서 모든 관리 되는 응용 프로그램 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="964bd-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="964bd-111">이 명령은 리소스 그룹 "MyRG"에서 관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="964bd-112">예제 2: 관리 되는 응용 프로그램 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="964bd-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="964bd-113">이 명령은 리소스 그룹 "MyRG"의 관리 되는 응용 프로그램 정의 "myManagedAppDef"를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="964bd-114">변수</span><span class="sxs-lookup"><span data-stu-id="964bd-114">PARAMETERS</span></span>

### <span data-ttu-id="964bd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="964bd-115">-ApiVersion</span></span>
<span data-ttu-id="964bd-116">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="964bd-117">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="964bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964bd-118">-DefaultProfile</span></span>
<span data-ttu-id="964bd-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="964bd-120">-Id</span><span class="sxs-lookup"><span data-stu-id="964bd-120">-Id</span></span>
<span data-ttu-id="964bd-121">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="964bd-122">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="964bd-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="964bd-123">-이름</span><span class="sxs-lookup"><span data-stu-id="964bd-123">-Name</span></span>
<span data-ttu-id="964bd-124">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="964bd-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="964bd-125">-Pre</span></span>
<span data-ttu-id="964bd-126">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="964bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="964bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="964bd-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-128">The resource group name.</span></span>

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

### <span data-ttu-id="964bd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964bd-129">CommonParameters</span></span>
<span data-ttu-id="964bd-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="964bd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964bd-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="964bd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964bd-132">입력</span><span class="sxs-lookup"><span data-stu-id="964bd-132">INPUTS</span></span>

### <span data-ttu-id="964bd-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="964bd-133">System.String</span></span>

## <span data-ttu-id="964bd-134">출력</span><span class="sxs-lookup"><span data-stu-id="964bd-134">OUTPUTS</span></span>

### <span data-ttu-id="964bd-135">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="964bd-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="964bd-136">상속자</span><span class="sxs-lookup"><span data-stu-id="964bd-136">NOTES</span></span>

## <span data-ttu-id="964bd-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="964bd-137">RELATED LINKS</span></span>
