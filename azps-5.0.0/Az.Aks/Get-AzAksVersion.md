---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217115"
---
# <span data-ttu-id="14c63-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="14c63-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="14c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c63-102">SYNOPSIS</span></span>
<span data-ttu-id="14c63-103">관리 되는 Kubernetes 클러스터를 만드는 데 사용할 수 있는 버전 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c63-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="14c63-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14c63-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c63-105">설명은</span><span class="sxs-lookup"><span data-stu-id="14c63-105">DESCRIPTION</span></span>
<span data-ttu-id="14c63-106">관리 되는 Kubernetes 클러스터를 만드는 데 사용할 수 있는 버전 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c63-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="14c63-107">예제의</span><span class="sxs-lookup"><span data-stu-id="14c63-107">EXAMPLES</span></span>

### <span data-ttu-id="14c63-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="14c63-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="14c63-109">변수</span><span class="sxs-lookup"><span data-stu-id="14c63-109">PARAMETERS</span></span>

### <span data-ttu-id="14c63-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c63-110">-DefaultProfile</span></span>
<span data-ttu-id="14c63-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14c63-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14c63-112">-위치</span><span class="sxs-lookup"><span data-stu-id="14c63-112">-Location</span></span>
<span data-ttu-id="14c63-113">클러스터에 대 한 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="14c63-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="14c63-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c63-114">CommonParameters</span></span>
<span data-ttu-id="14c63-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14c63-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c63-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14c63-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c63-117">입력</span><span class="sxs-lookup"><span data-stu-id="14c63-117">INPUTS</span></span>

### <span data-ttu-id="14c63-118">않아야</span><span class="sxs-lookup"><span data-stu-id="14c63-118">None</span></span>

## <span data-ttu-id="14c63-119">출력</span><span class="sxs-lookup"><span data-stu-id="14c63-119">OUTPUTS</span></span>

### <span data-ttu-id="14c63-120">Aks. PSOrchestratorVersionProfile/.</span><span class="sxs-lookup"><span data-stu-id="14c63-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="14c63-121">상속자</span><span class="sxs-lookup"><span data-stu-id="14c63-121">NOTES</span></span>

## <span data-ttu-id="14c63-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14c63-122">RELATED LINKS</span></span>
