---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: b2bd8855d9c8b125b4bef72f42f0bd4a63071adb
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93538280"
---
# <span data-ttu-id="65bdc-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="65bdc-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="65bdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="65bdc-103">작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65bdc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65bdc-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65bdc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="65bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="65bdc-106">**AzureRmOperationalInsightsWorkspace** cmdlet은 기존 작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="65bdc-107">작업 영역 이름을 지정 하는 경우이 cmdlet은 해당 작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="65bdc-108">이름을 지정 하지 않으면이 cmdlet은 리소스 그룹의 모든 작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="65bdc-109">이름과 리소스 그룹을 지정 하지 않으면이 cmdlet은 구독의 모든 작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="65bdc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="65bdc-110">EXAMPLES</span></span>

### <span data-ttu-id="65bdc-111">예제 1: 이름으로 작업 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="65bdc-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="65bdc-112">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 MyWorkspace 라는 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="65bdc-113">변수</span><span class="sxs-lookup"><span data-stu-id="65bdc-113">PARAMETERS</span></span>

### <span data-ttu-id="65bdc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65bdc-114">-DefaultProfile</span></span>
<span data-ttu-id="65bdc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="65bdc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65bdc-116">-이름</span><span class="sxs-lookup"><span data-stu-id="65bdc-116">-Name</span></span>
<span data-ttu-id="65bdc-117">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-117">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65bdc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65bdc-118">-ResourceGroupName</span></span>
<span data-ttu-id="65bdc-119">Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65bdc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65bdc-120">CommonParameters</span></span>
<span data-ttu-id="65bdc-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65bdc-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65bdc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65bdc-123">입력</span><span class="sxs-lookup"><span data-stu-id="65bdc-123">INPUTS</span></span>

### <span data-ttu-id="65bdc-124">않아야</span><span class="sxs-lookup"><span data-stu-id="65bdc-124">None</span></span>
<span data-ttu-id="65bdc-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65bdc-126">출력</span><span class="sxs-lookup"><span data-stu-id="65bdc-126">OUTPUTS</span></span>

### <span data-ttu-id="65bdc-127">OperationalInsights의 ' 1 [Microsoft Azure.] 목록에 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65bdc-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="65bdc-128">OperationalInsights. m a m/작업 영역</span><span class="sxs-lookup"><span data-stu-id="65bdc-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="65bdc-129">상속자</span><span class="sxs-lookup"><span data-stu-id="65bdc-129">NOTES</span></span>

## <span data-ttu-id="65bdc-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65bdc-130">RELATED LINKS</span></span>

[<span data-ttu-id="65bdc-131">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="65bdc-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


