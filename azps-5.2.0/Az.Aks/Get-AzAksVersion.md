---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356511"
---
# <span data-ttu-id="8e49b-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="8e49b-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="8e49b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e49b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e49b-103">관리되는 Kubernetes 클러스터를 만드는 데 사용할 수 있는 버전을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8e49b-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="8e49b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e49b-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e49b-105">설명</span><span class="sxs-lookup"><span data-stu-id="8e49b-105">DESCRIPTION</span></span>
<span data-ttu-id="8e49b-106">관리되는 Kubernetes 클러스터를 만드는 데 사용할 수 있는 버전을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8e49b-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="8e49b-107">예제</span><span class="sxs-lookup"><span data-stu-id="8e49b-107">EXAMPLES</span></span>

### <span data-ttu-id="8e49b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e49b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="8e49b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e49b-109">PARAMETERS</span></span>

### <span data-ttu-id="8e49b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e49b-110">-DefaultProfile</span></span>
<span data-ttu-id="8e49b-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e49b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e49b-112">-Location</span><span class="sxs-lookup"><span data-stu-id="8e49b-112">-Location</span></span>
<span data-ttu-id="8e49b-113">클러스터에 대한 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8e49b-113">Azure location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e49b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e49b-114">CommonParameters</span></span>
<span data-ttu-id="8e49b-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e49b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e49b-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e49b-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e49b-117">입력</span><span class="sxs-lookup"><span data-stu-id="8e49b-117">INPUTS</span></span>

### <span data-ttu-id="8e49b-118">없음</span><span class="sxs-lookup"><span data-stu-id="8e49b-118">None</span></span>

## <span data-ttu-id="8e49b-119">출력</span><span class="sxs-lookup"><span data-stu-id="8e49b-119">OUTPUTS</span></span>

### <span data-ttu-id="8e49b-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="8e49b-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="8e49b-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e49b-121">NOTES</span></span>

## <span data-ttu-id="8e49b-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e49b-122">RELATED LINKS</span></span>