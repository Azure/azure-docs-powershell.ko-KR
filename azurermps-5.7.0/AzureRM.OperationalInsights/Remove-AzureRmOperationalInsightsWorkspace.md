---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: d35797c007702f66bd462281a2531055524aeff5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703563"
---
# <span data-ttu-id="b4044-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4044-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="b4044-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4044-102">SYNOPSIS</span></span>
<span data-ttu-id="b4044-103">작업 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4044-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4044-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4044-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4044-105">DESCRIPTION</span></span>
<span data-ttu-id="b4044-106">**AzureRmOperationalInsightsWorkspace** cmdlet은 기존 작업 영역을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="b4044-107">이 작업 영역이 만든 시간에 *CustomerId* 매개 변수를 통해 기존 계정에 연결 된 경우에는 Operational Insights 포털에서 원래 계정이 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="b4044-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b4044-108">EXAMPLES</span></span>

### <span data-ttu-id="b4044-109">예제 1: 이름으로 작업 영역 제거</span><span class="sxs-lookup"><span data-stu-id="b4044-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="b4044-110">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="b4044-111">예제 2: 파이프라인을 사용 하 여 작업 영역을 제거 하 고 확인 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="b4044-112">이 명령은 Get-AzureRmOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져오고 파이프라인 연산자를 사용 하 여 제거를 **AzureRmOperationalInsightsWorkspace** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="b4044-113">*Force* 매개 변수를 지정 했기 때문에 명령에서 작업 영역을 제거 하기 전에 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="b4044-114">변수</span><span class="sxs-lookup"><span data-stu-id="b4044-114">PARAMETERS</span></span>

### <span data-ttu-id="b4044-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4044-115">-DefaultProfile</span></span>
<span data-ttu-id="b4044-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b4044-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4044-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b4044-117">-Force</span></span>
<span data-ttu-id="b4044-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4044-119">-이름</span><span class="sxs-lookup"><span data-stu-id="b4044-119">-Name</span></span>
<span data-ttu-id="b4044-120">작업 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="b4044-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4044-121">-ResourceGroupName</span></span>
<span data-ttu-id="b4044-122">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="b4044-123">-확인</span><span class="sxs-lookup"><span data-stu-id="b4044-123">-Confirm</span></span>
<span data-ttu-id="b4044-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4044-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4044-125">-WhatIf</span></span>
<span data-ttu-id="b4044-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4044-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4044-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4044-128">CommonParameters</span></span>
<span data-ttu-id="b4044-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4044-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4044-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4044-131">입력</span><span class="sxs-lookup"><span data-stu-id="b4044-131">INPUTS</span></span>

### <span data-ttu-id="b4044-132">않아야</span><span class="sxs-lookup"><span data-stu-id="b4044-132">None</span></span>
<span data-ttu-id="b4044-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4044-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4044-134">출력</span><span class="sxs-lookup"><span data-stu-id="b4044-134">OUTPUTS</span></span>

## <span data-ttu-id="b4044-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b4044-135">NOTES</span></span>

## <span data-ttu-id="b4044-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4044-136">RELATED LINKS</span></span>

[<span data-ttu-id="b4044-137">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b4044-137">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="b4044-138">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b4044-138">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


