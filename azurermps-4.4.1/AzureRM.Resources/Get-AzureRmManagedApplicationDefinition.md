---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ef724c4d2e9771243058471c3ce2aebc944d2bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702412"
---
# <span data-ttu-id="34850-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="34850-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="34850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34850-102">SYNOPSIS</span></span>
<span data-ttu-id="34850-103">관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34850-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34850-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34850-104">SYNTAX</span></span>

### <span data-ttu-id="34850-105">관리 되는 응용 프로그램 정의 이름 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="34850-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="34850-106">기본값</span><span class="sxs-lookup"><span data-stu-id="34850-106">(Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34850-107">관리 되는 응용 프로그램 정의 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="34850-107">The managed application definition Id parameter set.</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34850-108">설명은</span><span class="sxs-lookup"><span data-stu-id="34850-108">DESCRIPTION</span></span>
<span data-ttu-id="34850-109">**Get-AzureRmManagedApplicationDefinition** cmdlet은 관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34850-109">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="34850-110">예제의</span><span class="sxs-lookup"><span data-stu-id="34850-110">EXAMPLES</span></span>

### <span data-ttu-id="34850-111">예제 1: 리소스 그룹에서 모든 관리 되는 응용 프로그램 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="34850-111">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="34850-112">이 명령은 리소스 그룹 "MyRG"에서 관리 되는 응용 프로그램 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34850-112">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="34850-113">예제 2: 관리 되는 응용 프로그램 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="34850-113">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="34850-114">이 명령은 리소스 그룹 "MyRG"의 관리 되는 응용 프로그램 정의 "myManagedAppDef"를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="34850-114">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="34850-115">변수</span><span class="sxs-lookup"><span data-stu-id="34850-115">PARAMETERS</span></span>

### <span data-ttu-id="34850-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="34850-116">-ApiVersion</span></span>
<span data-ttu-id="34850-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="34850-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="34850-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34850-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="34850-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34850-119">-DefaultProfile</span></span>
<span data-ttu-id="34850-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34850-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34850-121">-Id</span><span class="sxs-lookup"><span data-stu-id="34850-121">-Id</span></span>
<span data-ttu-id="34850-122">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="34850-122">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="34850-123">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="34850-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34850-124">-이름</span><span class="sxs-lookup"><span data-stu-id="34850-124">-Name</span></span>
<span data-ttu-id="34850-125">관리 되는 응용 프로그램 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34850-125">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34850-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="34850-126">-Pre</span></span>
<span data-ttu-id="34850-127">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="34850-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="34850-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34850-128">-ResourceGroupName</span></span>
<span data-ttu-id="34850-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34850-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34850-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34850-130">CommonParameters</span></span>
<span data-ttu-id="34850-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34850-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34850-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34850-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34850-133">입력</span><span class="sxs-lookup"><span data-stu-id="34850-133">INPUTS</span></span>

### <span data-ttu-id="34850-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="34850-134">System.String</span></span>

## <span data-ttu-id="34850-135">출력</span><span class="sxs-lookup"><span data-stu-id="34850-135">OUTPUTS</span></span>

### <span data-ttu-id="34850-136">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="34850-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="34850-137">상속자</span><span class="sxs-lookup"><span data-stu-id="34850-137">NOTES</span></span>

## <span data-ttu-id="34850-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34850-138">RELATED LINKS</span></span>

