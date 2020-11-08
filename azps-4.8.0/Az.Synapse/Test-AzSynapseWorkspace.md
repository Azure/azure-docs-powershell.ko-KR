---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213456"
---
# <span data-ttu-id="256de-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="256de-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="256de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="256de-102">SYNOPSIS</span></span>
<span data-ttu-id="256de-103">Synapse Analytics 작업 영역이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="256de-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="256de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="256de-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="256de-105">설명은</span><span class="sxs-lookup"><span data-stu-id="256de-105">DESCRIPTION</span></span>
<span data-ttu-id="256de-106">**AzSynapseWorkspace** Cmdlet은 Synapse Analytics 작업 영역이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="256de-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="256de-107">예제의</span><span class="sxs-lookup"><span data-stu-id="256de-107">EXAMPLES</span></span>

### <span data-ttu-id="256de-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="256de-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="256de-109">이 명령은 Synapse Analytics 작업 영역이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="256de-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="256de-110">변수</span><span class="sxs-lookup"><span data-stu-id="256de-110">PARAMETERS</span></span>

### <span data-ttu-id="256de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="256de-111">-DefaultProfile</span></span>
<span data-ttu-id="256de-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="256de-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="256de-113">-이름</span><span class="sxs-lookup"><span data-stu-id="256de-113">-Name</span></span>
<span data-ttu-id="256de-114">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="256de-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256de-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="256de-115">-ResourceGroupName</span></span>
<span data-ttu-id="256de-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="256de-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="256de-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="256de-117">CommonParameters</span></span>
<span data-ttu-id="256de-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="256de-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="256de-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="256de-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="256de-120">입력</span><span class="sxs-lookup"><span data-stu-id="256de-120">INPUTS</span></span>

### <span data-ttu-id="256de-121">않아야</span><span class="sxs-lookup"><span data-stu-id="256de-121">None</span></span>

## <span data-ttu-id="256de-122">출력</span><span class="sxs-lookup"><span data-stu-id="256de-122">OUTPUTS</span></span>

### <span data-ttu-id="256de-123">System. 개체</span><span class="sxs-lookup"><span data-stu-id="256de-123">System.Object</span></span>
## <span data-ttu-id="256de-124">상속자</span><span class="sxs-lookup"><span data-stu-id="256de-124">NOTES</span></span>

## <span data-ttu-id="256de-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="256de-125">RELATED LINKS</span></span>
