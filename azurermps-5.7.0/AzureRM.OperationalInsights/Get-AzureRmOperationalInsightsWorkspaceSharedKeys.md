---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 5fab6a3a0419047fef32f5bf32f52e1f7ee57d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528007"
---
# <span data-ttu-id="aad6c-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="aad6c-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="aad6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aad6c-102">SYNOPSIS</span></span>
<span data-ttu-id="aad6c-103">작업 영역의 공유 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aad6c-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aad6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aad6c-105">DESCRIPTION</span></span>
<span data-ttu-id="aad6c-106">**AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet은 작업 영역의 공유 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="aad6c-107">키를 사용 하 여 Operational Insights 에이전트를 작업 영역에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="aad6c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="aad6c-108">EXAMPLES</span></span>

### <span data-ttu-id="aad6c-109">예제 1: 작업 영역 이름으로 공유 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="aad6c-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="aad6c-110">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역의 공유 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="aad6c-111">예제 2: 파이프라인을 사용 하 여 공유 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="aad6c-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="aad6c-112">이 명령은 Get-AzureRmOperationalInsightsWorkspace cmdlet을 사용 하 여 MyWorkspace 라는 작업 영역을 가져온 다음 작업 영역을 **AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="aad6c-113">명령은 해당 작업 영역의 공유 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="aad6c-114">변수</span><span class="sxs-lookup"><span data-stu-id="aad6c-114">PARAMETERS</span></span>

### <span data-ttu-id="aad6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad6c-115">-DefaultProfile</span></span>
<span data-ttu-id="aad6c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aad6c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aad6c-117">-이름</span><span class="sxs-lookup"><span data-stu-id="aad6c-117">-Name</span></span>
<span data-ttu-id="aad6c-118">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="aad6c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad6c-119">-ResourceGroupName</span></span>
<span data-ttu-id="aad6c-120">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="aad6c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad6c-121">CommonParameters</span></span>
<span data-ttu-id="aad6c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad6c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad6c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad6c-124">입력</span><span class="sxs-lookup"><span data-stu-id="aad6c-124">INPUTS</span></span>

### <span data-ttu-id="aad6c-125">않아야</span><span class="sxs-lookup"><span data-stu-id="aad6c-125">None</span></span>
<span data-ttu-id="aad6c-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aad6c-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aad6c-127">출력</span><span class="sxs-lookup"><span data-stu-id="aad6c-127">OUTPUTS</span></span>

### <span data-ttu-id="aad6c-128">OperationalInsights. PSWorkspaceKeys/.</span><span class="sxs-lookup"><span data-stu-id="aad6c-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="aad6c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="aad6c-129">NOTES</span></span>

## <span data-ttu-id="aad6c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aad6c-130">RELATED LINKS</span></span>

[<span data-ttu-id="aad6c-131">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aad6c-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="aad6c-132">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="aad6c-132">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


