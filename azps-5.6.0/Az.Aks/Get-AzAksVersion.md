---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 3a46f28ad0f169f4f4f280922dff675b5e749fed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966896"
---
# <span data-ttu-id="30f4f-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="30f4f-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="30f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="30f4f-103">관리되는 Kubernetes 클러스터를 만드는 데 사용할 수 있는 버전을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="30f4f-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="30f4f-104">구문</span><span class="sxs-lookup"><span data-stu-id="30f4f-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30f4f-105">설명</span><span class="sxs-lookup"><span data-stu-id="30f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="30f4f-106">관리되는 Kubernetes 클러스터를 만드는 데 사용할 수 있는 버전을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="30f4f-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="30f4f-107">예제</span><span class="sxs-lookup"><span data-stu-id="30f4f-107">EXAMPLES</span></span>

### <span data-ttu-id="30f4f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="30f4f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="30f4f-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="30f4f-109">PARAMETERS</span></span>

### <span data-ttu-id="30f4f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f4f-110">-DefaultProfile</span></span>
<span data-ttu-id="30f4f-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30f4f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30f4f-112">-Location</span><span class="sxs-lookup"><span data-stu-id="30f4f-112">-Location</span></span>
<span data-ttu-id="30f4f-113">클러스터의 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="30f4f-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="30f4f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f4f-114">CommonParameters</span></span>
<span data-ttu-id="30f4f-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30f4f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f4f-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30f4f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f4f-117">입력</span><span class="sxs-lookup"><span data-stu-id="30f4f-117">INPUTS</span></span>

### <span data-ttu-id="30f4f-118">없음</span><span class="sxs-lookup"><span data-stu-id="30f4f-118">None</span></span>

## <span data-ttu-id="30f4f-119">출력</span><span class="sxs-lookup"><span data-stu-id="30f4f-119">OUTPUTS</span></span>

### <span data-ttu-id="30f4f-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="30f4f-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="30f4f-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30f4f-121">NOTES</span></span>

## <span data-ttu-id="30f4f-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30f4f-122">RELATED LINKS</span></span>
