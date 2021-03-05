---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: e92b4d20e89df451c483bc0b4bdccb83fdc8a140
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011200"
---
# <span data-ttu-id="5c897-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5c897-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="5c897-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c897-102">SYNOPSIS</span></span>
<span data-ttu-id="5c897-103">Synapse Analytics 작업 영역의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="5c897-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="5c897-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c897-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c897-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c897-105">DESCRIPTION</span></span>
<span data-ttu-id="5c897-106">**Test-AzSynapseWorkspace** cmdlet은 Synapse Analytics 작업 영역의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="5c897-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="5c897-107">예제</span><span class="sxs-lookup"><span data-stu-id="5c897-107">EXAMPLES</span></span>

### <span data-ttu-id="5c897-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c897-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="5c897-109">이 명령은 Synapse Analytics 작업 영역의 존재를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="5c897-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="5c897-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c897-110">PARAMETERS</span></span>

### <span data-ttu-id="5c897-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c897-111">-DefaultProfile</span></span>
<span data-ttu-id="5c897-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c897-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c897-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5c897-113">-Name</span></span>
<span data-ttu-id="5c897-114">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c897-114">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5c897-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c897-115">-ResourceGroupName</span></span>
<span data-ttu-id="5c897-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c897-116">Resource group name.</span></span>

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

### <span data-ttu-id="5c897-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c897-117">CommonParameters</span></span>
<span data-ttu-id="5c897-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c897-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c897-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c897-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c897-120">입력</span><span class="sxs-lookup"><span data-stu-id="5c897-120">INPUTS</span></span>

### <span data-ttu-id="5c897-121">없음</span><span class="sxs-lookup"><span data-stu-id="5c897-121">None</span></span>

## <span data-ttu-id="5c897-122">출력</span><span class="sxs-lookup"><span data-stu-id="5c897-122">OUTPUTS</span></span>

### <span data-ttu-id="5c897-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="5c897-123">System.Object</span></span>
## <span data-ttu-id="5c897-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c897-124">NOTES</span></span>

## <span data-ttu-id="5c897-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c897-125">RELATED LINKS</span></span>
