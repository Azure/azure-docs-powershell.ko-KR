---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339818"
---
# <span data-ttu-id="57111-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="57111-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="57111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57111-102">SYNOPSIS</span></span>
<span data-ttu-id="57111-103">Synapse Analytics 작업 영역의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="57111-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="57111-104">구문</span><span class="sxs-lookup"><span data-stu-id="57111-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57111-105">설명</span><span class="sxs-lookup"><span data-stu-id="57111-105">DESCRIPTION</span></span>
<span data-ttu-id="57111-106">**Test-AzSynapseWorkspace** cmdlet은 Synapse Analytics 작업 영역의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="57111-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="57111-107">예제</span><span class="sxs-lookup"><span data-stu-id="57111-107">EXAMPLES</span></span>

### <span data-ttu-id="57111-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="57111-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="57111-109">이 명령은 Synapse Analytics 작업 영역의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="57111-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="57111-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57111-110">PARAMETERS</span></span>

### <span data-ttu-id="57111-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57111-111">-DefaultProfile</span></span>
<span data-ttu-id="57111-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57111-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57111-113">-Name</span><span class="sxs-lookup"><span data-stu-id="57111-113">-Name</span></span>
<span data-ttu-id="57111-114">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57111-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="57111-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57111-115">-ResourceGroupName</span></span>
<span data-ttu-id="57111-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57111-116">Resource group name.</span></span>

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

### <span data-ttu-id="57111-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57111-117">CommonParameters</span></span>
<span data-ttu-id="57111-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57111-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57111-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57111-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57111-120">입력</span><span class="sxs-lookup"><span data-stu-id="57111-120">INPUTS</span></span>

### <span data-ttu-id="57111-121">없음</span><span class="sxs-lookup"><span data-stu-id="57111-121">None</span></span>

## <span data-ttu-id="57111-122">출력</span><span class="sxs-lookup"><span data-stu-id="57111-122">OUTPUTS</span></span>

### <span data-ttu-id="57111-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="57111-123">System.Object</span></span>
## <span data-ttu-id="57111-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57111-124">NOTES</span></span>

## <span data-ttu-id="57111-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57111-125">RELATED LINKS</span></span>
