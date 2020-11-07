---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: e6df93dee8599c6bae42cc9428b2a7691abf4740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881758"
---
# <span data-ttu-id="9aea6-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="9aea6-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="9aea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aea6-102">SYNOPSIS</span></span>
<span data-ttu-id="9aea6-103">관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aea6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9aea6-104">SYNTAX</span></span>

### <span data-ttu-id="9aea6-105">GetByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="9aea6-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aea6-106">GetById</span><span class="sxs-lookup"><span data-stu-id="9aea6-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9aea6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9aea6-107">DESCRIPTION</span></span>
<span data-ttu-id="9aea6-108">**Get-AzureRmManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="9aea6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9aea6-109">EXAMPLES</span></span>

### <span data-ttu-id="9aea6-110">예제 1: 리소스 그룹에서 모든 관리 되는 응용 프로그램 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="9aea6-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="9aea6-111">이 명령은 리소스 그룹 "MyRG"에서 관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="9aea6-112">예제 2: 관리 되는 응용 프로그램 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="9aea6-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="9aea6-113">이 명령은 리소스 그룹 "MyRG"의 관리 되는 응용 프로그램 정의 "myManagedAppDef"를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="9aea6-114">변수</span><span class="sxs-lookup"><span data-stu-id="9aea6-114">PARAMETERS</span></span>

### <span data-ttu-id="9aea6-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9aea6-115">-ApiVersion</span></span>
<span data-ttu-id="9aea6-116">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9aea6-117">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aea6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aea6-118">-DefaultProfile</span></span>
<span data-ttu-id="9aea6-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aea6-120">-Id</span><span class="sxs-lookup"><span data-stu-id="9aea6-120">-Id</span></span>
<span data-ttu-id="9aea6-121">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="9aea6-122">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="9aea6-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aea6-123">-이름</span><span class="sxs-lookup"><span data-stu-id="9aea6-123">-Name</span></span>
<span data-ttu-id="9aea6-124">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-124">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aea6-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="9aea6-125">-Pre</span></span>
<span data-ttu-id="9aea6-126">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9aea6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aea6-127">-ResourceGroupName</span></span>
<span data-ttu-id="9aea6-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aea6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aea6-129">CommonParameters</span></span>
<span data-ttu-id="9aea6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aea6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aea6-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aea6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aea6-132">입력</span><span class="sxs-lookup"><span data-stu-id="9aea6-132">INPUTS</span></span>

### <span data-ttu-id="9aea6-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9aea6-133">System.String</span></span>

## <span data-ttu-id="9aea6-134">출력</span><span class="sxs-lookup"><span data-stu-id="9aea6-134">OUTPUTS</span></span>

### <span data-ttu-id="9aea6-135">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="9aea6-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9aea6-136">상속자</span><span class="sxs-lookup"><span data-stu-id="9aea6-136">NOTES</span></span>

## <span data-ttu-id="9aea6-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9aea6-137">RELATED LINKS</span></span>
