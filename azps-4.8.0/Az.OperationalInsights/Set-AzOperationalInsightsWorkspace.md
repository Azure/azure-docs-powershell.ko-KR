---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212942"
---
# <span data-ttu-id="acaa5-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="acaa5-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="acaa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acaa5-102">SYNOPSIS</span></span>
<span data-ttu-id="acaa5-103">작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-103">Updates a workspace.</span></span>

## <span data-ttu-id="acaa5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="acaa5-104">SYNTAX</span></span>

### <span data-ttu-id="acaa5-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="acaa5-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="acaa5-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="acaa5-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="acaa5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="acaa5-107">DESCRIPTION</span></span>
<span data-ttu-id="acaa5-108">**AzOperationalInsightsWorkspace** cmdlet은 작업 영역의 구성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="acaa5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="acaa5-109">EXAMPLES</span></span>

### <span data-ttu-id="acaa5-110">예제 1: 이름으로 작업 영역 수정</span><span class="sxs-lookup"><span data-stu-id="acaa5-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="acaa5-111">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역의 SKU와 태그를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="acaa5-112">예제 2: 파이프라인을 사용 하 여 작업 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="acaa5-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="acaa5-113">이 명령은 Get-AzOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkSpace 라는 작업 영역을 가져오고 파이프라인 연산자를 사용 하 여 SKU에서 Premium으로 설정 하 여 **AzOperationalInsightsWorkspace** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="acaa5-114">변수</span><span class="sxs-lookup"><span data-stu-id="acaa5-114">PARAMETERS</span></span>

### <span data-ttu-id="acaa5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acaa5-115">-DefaultProfile</span></span>
<span data-ttu-id="acaa5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="acaa5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acaa5-117">-이름</span><span class="sxs-lookup"><span data-stu-id="acaa5-117">-Name</span></span>
<span data-ttu-id="acaa5-118">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="acaa5-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="acaa5-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="acaa5-120">작업 영역 수집에 액세스 하는 데 사용 되는 네트워크 액세스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="acaa5-121">값은 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="acaa5-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="acaa5-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="acaa5-123">작업 영역 쿼리에 액세스 하는 데 사용 되는 네트워크 액세스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="acaa5-124">값은 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="acaa5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acaa5-125">-ResourceGroupName</span></span>
<span data-ttu-id="acaa5-126">Azure 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-126">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="acaa5-127">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="acaa5-127">-RetentionInDays</span></span>
<span data-ttu-id="acaa5-128">작업 영역 데이터 보존 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-128">The workspace data retention in days.</span></span> <span data-ttu-id="acaa5-129">730 일이 다른 모든 Sku에 허용 되는 최대값입니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-129">730 days is the maximum allowed for all other Skus</span></span>

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

### <span data-ttu-id="acaa5-130">-Sku</span><span class="sxs-lookup"><span data-stu-id="acaa5-130">-Sku</span></span>
<span data-ttu-id="acaa5-131">작업 영역의 서비스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="acaa5-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-132">Valid values are:</span></span> 
- <span data-ttu-id="acaa5-133">비우거나</span><span class="sxs-lookup"><span data-stu-id="acaa5-133">free</span></span>
- <span data-ttu-id="acaa5-134">표준이</span><span class="sxs-lookup"><span data-stu-id="acaa5-134">standard</span></span>
- <span data-ttu-id="acaa5-135">premium</span><span class="sxs-lookup"><span data-stu-id="acaa5-135">premium</span></span>
- <span data-ttu-id="acaa5-136">pernode</span><span class="sxs-lookup"><span data-stu-id="acaa5-136">pernode</span></span>
- <span data-ttu-id="acaa5-137">독립</span><span class="sxs-lookup"><span data-stu-id="acaa5-137">standalone</span></span>
- <span data-ttu-id="acaa5-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="acaa5-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acaa5-139">태그</span><span class="sxs-lookup"><span data-stu-id="acaa5-139">-Tag</span></span>
<span data-ttu-id="acaa5-140">작업 영역의 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-140">The resource tags for the workspace.</span></span>

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

### <span data-ttu-id="acaa5-141">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="acaa5-141">-Workspace</span></span>
<span data-ttu-id="acaa5-142">업데이트할 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-142">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="acaa5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acaa5-143">CommonParameters</span></span>
<span data-ttu-id="acaa5-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="acaa5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acaa5-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="acaa5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acaa5-146">입력</span><span class="sxs-lookup"><span data-stu-id="acaa5-146">INPUTS</span></span>

### <span data-ttu-id="acaa5-147">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="acaa5-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="acaa5-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="acaa5-148">System.String</span></span>

### <span data-ttu-id="acaa5-149">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="acaa5-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="acaa5-150">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="acaa5-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="acaa5-151">출력</span><span class="sxs-lookup"><span data-stu-id="acaa5-151">OUTPUTS</span></span>

### <span data-ttu-id="acaa5-152">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="acaa5-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="acaa5-153">상속자</span><span class="sxs-lookup"><span data-stu-id="acaa5-153">NOTES</span></span>

## <span data-ttu-id="acaa5-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acaa5-154">RELATED LINKS</span></span>

[<span data-ttu-id="acaa5-155">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="acaa5-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="acaa5-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="acaa5-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


