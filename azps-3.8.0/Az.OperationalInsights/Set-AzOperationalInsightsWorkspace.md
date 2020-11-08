---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 3d85bcbf5352c06e379ac317cde052f3e744c10d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94047279"
---
# <span data-ttu-id="c96fd-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c96fd-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="c96fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c96fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c96fd-103">작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-103">Updates a workspace.</span></span>

## <span data-ttu-id="c96fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c96fd-104">SYNTAX</span></span>

### <span data-ttu-id="c96fd-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c96fd-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c96fd-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c96fd-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c96fd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c96fd-107">DESCRIPTION</span></span>
<span data-ttu-id="c96fd-108">**AzOperationalInsightsWorkspace** cmdlet은 작업 영역의 구성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="c96fd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c96fd-109">EXAMPLES</span></span>

### <span data-ttu-id="c96fd-110">예제 1: 이름으로 작업 영역 수정</span><span class="sxs-lookup"><span data-stu-id="c96fd-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="c96fd-111">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역의 SKU와 태그를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c96fd-112">예제 2: 파이프라인을 사용 하 여 작업 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="c96fd-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="c96fd-113">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkSpace 라는 작업 영역을 가져오고 파이프라인 연산자를 사용 하 여 SKU에서 Premium으로 설정 하 여 **AzOperationalInsightsWorkspace** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="c96fd-114">변수</span><span class="sxs-lookup"><span data-stu-id="c96fd-114">PARAMETERS</span></span>

### <span data-ttu-id="c96fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c96fd-115">-DefaultProfile</span></span>
<span data-ttu-id="c96fd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c96fd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c96fd-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c96fd-117">-Name</span></span>
<span data-ttu-id="c96fd-118">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96fd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c96fd-119">-ResourceGroupName</span></span>
<span data-ttu-id="c96fd-120">Azure 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-120">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96fd-121">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="c96fd-121">-RetentionInDays</span></span>
<span data-ttu-id="c96fd-122">작업 영역 데이터 보존 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-122">The workspace data retention in days.</span></span> <span data-ttu-id="c96fd-123">730 일이 다른 모든 Sku에 허용 되는 최대값입니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-123">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96fd-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="c96fd-124">-Sku</span></span>
<span data-ttu-id="c96fd-125">작업 영역의 서비스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-125">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="c96fd-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-126">Valid values are:</span></span> 
- <span data-ttu-id="c96fd-127">비우거나</span><span class="sxs-lookup"><span data-stu-id="c96fd-127">free</span></span>
- <span data-ttu-id="c96fd-128">표준이</span><span class="sxs-lookup"><span data-stu-id="c96fd-128">standard</span></span>
- <span data-ttu-id="c96fd-129">premium</span><span class="sxs-lookup"><span data-stu-id="c96fd-129">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96fd-130">태그</span><span class="sxs-lookup"><span data-stu-id="c96fd-130">-Tag</span></span>
<span data-ttu-id="c96fd-131">작업 영역의 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-131">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c96fd-132">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="c96fd-132">-Workspace</span></span>
<span data-ttu-id="c96fd-133">업데이트할 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-133">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c96fd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96fd-134">CommonParameters</span></span>
<span data-ttu-id="c96fd-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c96fd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96fd-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c96fd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96fd-137">입력</span><span class="sxs-lookup"><span data-stu-id="c96fd-137">INPUTS</span></span>

### <span data-ttu-id="c96fd-138">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="c96fd-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c96fd-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c96fd-139">System.String</span></span>

### <span data-ttu-id="c96fd-140">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="c96fd-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c96fd-141">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="c96fd-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c96fd-142">출력</span><span class="sxs-lookup"><span data-stu-id="c96fd-142">OUTPUTS</span></span>

### <span data-ttu-id="c96fd-143">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="c96fd-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="c96fd-144">상속자</span><span class="sxs-lookup"><span data-stu-id="c96fd-144">NOTES</span></span>

## <span data-ttu-id="c96fd-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c96fd-145">RELATED LINKS</span></span>

[<span data-ttu-id="c96fd-146">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c96fd-146">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="c96fd-147">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c96fd-147">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


