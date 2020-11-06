---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: e24597d25fffdc1b516c5a18cf011f7222d288c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527351"
---
# <span data-ttu-id="0773c-101">Set-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0773c-101">Set-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="0773c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0773c-102">SYNOPSIS</span></span>
<span data-ttu-id="0773c-103">작업 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-103">Updates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0773c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0773c-104">SYNTAX</span></span>

### <span data-ttu-id="0773c-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0773c-105">ByName (Default)</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tags] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0773c-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="0773c-106">ByObject</span></span>
```
Set-AzureRmOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tags] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0773c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0773c-107">DESCRIPTION</span></span>
<span data-ttu-id="0773c-108">**AzureRmOperationalInsightsWorkspace** cmdlet은 작업 영역의 구성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-108">The **Set-AzureRmOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="0773c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0773c-109">EXAMPLES</span></span>

### <span data-ttu-id="0773c-110">예제 1: 이름으로 작업 영역 수정</span><span class="sxs-lookup"><span data-stu-id="0773c-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="0773c-111">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역의 SKU와 태그를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="0773c-112">예제 2: 파이프라인을 사용 하 여 작업 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="0773c-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzureRmOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="0773c-113">이 명령은 Get-AzureRmOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkSpace 라는 작업 영역을 가져오고 파이프라인 연산자를 사용 하 여 SKU에서 Premium으로 설정 하 여 **AzureRmOperationalInsightsWorkspace** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-113">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="0773c-114">변수</span><span class="sxs-lookup"><span data-stu-id="0773c-114">PARAMETERS</span></span>

### <span data-ttu-id="0773c-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0773c-115">-Name</span></span>
<span data-ttu-id="0773c-116">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0773c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0773c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0773c-118">Azure 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-118">Specifies the Azure resource group name.</span></span>

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

### <span data-ttu-id="0773c-119">-Sku</span><span class="sxs-lookup"><span data-stu-id="0773c-119">-Sku</span></span>
<span data-ttu-id="0773c-120">작업 영역의 서비스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-120">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="0773c-121">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-121">Valid values are:</span></span> 

- <span data-ttu-id="0773c-122">비우거나</span><span class="sxs-lookup"><span data-stu-id="0773c-122">free</span></span>
- <span data-ttu-id="0773c-123">표준이</span><span class="sxs-lookup"><span data-stu-id="0773c-123">standard</span></span>
- <span data-ttu-id="0773c-124">premium</span><span class="sxs-lookup"><span data-stu-id="0773c-124">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: free, standard, premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0773c-125">태그</span><span class="sxs-lookup"><span data-stu-id="0773c-125">-Tags</span></span>
<span data-ttu-id="0773c-126">작업 영역의 리소스 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-126">Specifies the resource tags for the workspace.</span></span>

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

### <span data-ttu-id="0773c-127">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="0773c-127">-Workspace</span></span>
<span data-ttu-id="0773c-128">업데이트할 작업 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-128">Specifies the workspace to be updated.</span></span>

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

### <span data-ttu-id="0773c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0773c-129">-DefaultProfile</span></span>
<span data-ttu-id="0773c-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0773c-131">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="0773c-131">-RetentionInDays</span></span>
<span data-ttu-id="0773c-132">작업 영역 데이터 보존 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-132">The workspace data retention in days.</span></span> <span data-ttu-id="0773c-133">730 일은 다른 모든 Sku에 허용 되는 최대값입니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-133">730 days is the maximum allowed for all other Skus.</span></span>

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

### <span data-ttu-id="0773c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0773c-134">CommonParameters</span></span>
<span data-ttu-id="0773c-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0773c-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0773c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0773c-137">입력</span><span class="sxs-lookup"><span data-stu-id="0773c-137">INPUTS</span></span>

### <span data-ttu-id="0773c-138">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0773c-138">PSWorkspace</span></span>
<span data-ttu-id="0773c-139">' Workspace ' 매개 변수는 파이프라인에서 ' PSWorkspace ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0773c-139">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="0773c-140">출력</span><span class="sxs-lookup"><span data-stu-id="0773c-140">OUTPUTS</span></span>

### <span data-ttu-id="0773c-141">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="0773c-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="0773c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="0773c-142">NOTES</span></span>

## <span data-ttu-id="0773c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0773c-143">RELATED LINKS</span></span>

[<span data-ttu-id="0773c-144">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0773c-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="0773c-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0773c-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


