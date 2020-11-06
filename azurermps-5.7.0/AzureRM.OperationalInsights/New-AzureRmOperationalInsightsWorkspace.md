---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 0ba43a38763252275d7461f11cc4db574720ba5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531691"
---
# <span data-ttu-id="f47e0-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f47e0-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="f47e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f47e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f47e0-103">작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f47e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f47e0-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f47e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f47e0-105">DESCRIPTION</span></span>
<span data-ttu-id="f47e0-106">**AzureRmOperationalInsightsWorkspace** cmdlet은 지정 된 리소스 그룹 및 위치에 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="f47e0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f47e0-107">EXAMPLES</span></span>

### <span data-ttu-id="f47e0-108">예제 1: 이름으로 작업 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="f47e0-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="f47e0-109">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에 MyWorkspace 라는 표준 SKU 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="f47e0-110">예제 2: 작업 영역 만들기 및 기존 계정에 연결</span><span class="sxs-lookup"><span data-stu-id="f47e0-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="f47e0-111">첫 번째 명령은 Get-AzureRmOperationalInsightsLinkTargets cmdlet을 사용 하 여 Operational Insights 계정 링크 대상을 가져오고이를 $OILinkTargets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>

<span data-ttu-id="f47e0-112">두 번째 명령은 파이프라인 연산자를 사용 하 여 $OILinkTargets의 첫 번째 계정 링크 대상을 **새 AzureRmOperationalInsightsWorkspace** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f47e0-113">이 명령은 $OILinkTargets의 첫 번째 Operational Insights 계정에 연결 되는 MyWorkspace 라는 표준 SKU 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="f47e0-114">변수</span><span class="sxs-lookup"><span data-stu-id="f47e0-114">PARAMETERS</span></span>

### <span data-ttu-id="f47e0-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="f47e0-115">-CustomerId</span></span>
<span data-ttu-id="f47e0-116">이 작업 영역이 연결 될 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="f47e0-117">Get-AzureRmOperationalInsightsLinkTargets cmdlet을 사용 하 여 잠재적 계정을 나열할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f47e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47e0-118">-DefaultProfile</span></span>
<span data-ttu-id="f47e0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f47e0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f47e0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f47e0-120">-Force</span></span>
<span data-ttu-id="f47e0-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f47e0-122">-위치</span><span class="sxs-lookup"><span data-stu-id="f47e0-122">-Location</span></span>
<span data-ttu-id="f47e0-123">작업 영역을 만들 위치를 지정 합니다 (예: 동부 미국 또는 서유럽).</span><span class="sxs-lookup"><span data-stu-id="f47e0-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f47e0-124">-이름</span><span class="sxs-lookup"><span data-stu-id="f47e0-124">-Name</span></span>
<span data-ttu-id="f47e0-125">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-125">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f47e0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f47e0-126">-ResourceGroupName</span></span>
<span data-ttu-id="f47e0-127">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f47e0-128">이 리소스 그룹에 작업 영역이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-128">The workspace is created in this resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f47e0-129">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="f47e0-129">-RetentionInDays</span></span>
<span data-ttu-id="f47e0-130">작업 영역 데이터 보존 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-130">The workspace data retention in days.</span></span> <span data-ttu-id="f47e0-131">730 일이 다른 모든 Sku에 허용 되는 최대값입니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-131">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f47e0-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="f47e0-132">-Sku</span></span>
<span data-ttu-id="f47e0-133">작업 영역의 서비스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="f47e0-134">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-134">Valid values are:</span></span> 

- <span data-ttu-id="f47e0-135">비우거나</span><span class="sxs-lookup"><span data-stu-id="f47e0-135">free</span></span>
- <span data-ttu-id="f47e0-136">표준이</span><span class="sxs-lookup"><span data-stu-id="f47e0-136">standard</span></span>
- <span data-ttu-id="f47e0-137">premium</span><span class="sxs-lookup"><span data-stu-id="f47e0-137">premium</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f47e0-138">태그</span><span class="sxs-lookup"><span data-stu-id="f47e0-138">-Tag</span></span>
<span data-ttu-id="f47e0-139">작업 영역의 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-139">The resource tags for the workspace.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f47e0-140">-확인</span><span class="sxs-lookup"><span data-stu-id="f47e0-140">-Confirm</span></span>
<span data-ttu-id="f47e0-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47e0-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47e0-142">-WhatIf</span></span>
<span data-ttu-id="f47e0-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f47e0-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47e0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47e0-145">CommonParameters</span></span>
<span data-ttu-id="f47e0-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47e0-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f47e0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47e0-148">입력</span><span class="sxs-lookup"><span data-stu-id="f47e0-148">INPUTS</span></span>

### <span data-ttu-id="f47e0-149">않아야</span><span class="sxs-lookup"><span data-stu-id="f47e0-149">None</span></span>
<span data-ttu-id="f47e0-150">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f47e0-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f47e0-151">출력</span><span class="sxs-lookup"><span data-stu-id="f47e0-151">OUTPUTS</span></span>

### <span data-ttu-id="f47e0-152">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="f47e0-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="f47e0-153">상속자</span><span class="sxs-lookup"><span data-stu-id="f47e0-153">NOTES</span></span>

## <span data-ttu-id="f47e0-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f47e0-154">RELATED LINKS</span></span>

[<span data-ttu-id="f47e0-155">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f47e0-155">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="f47e0-156">Get-AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="f47e0-156">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


