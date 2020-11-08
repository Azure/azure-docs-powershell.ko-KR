---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213414"
---
# <span data-ttu-id="09f1b-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="09f1b-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="09f1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="09f1b-103">Kubernetes 관리 되는 클러스터 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09f1b-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="09f1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09f1b-104">SYNTAX</span></span>

### <span data-ttu-id="09f1b-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="09f1b-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09f1b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09f1b-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f1b-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09f1b-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09f1b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="09f1b-108">DESCRIPTION</span></span>
<span data-ttu-id="09f1b-109">Kubernetes 관리 되는 클러스터 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09f1b-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="09f1b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="09f1b-110">EXAMPLES</span></span>

### <span data-ttu-id="09f1b-111">모든 Kubernetes 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="09f1b-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="09f1b-112">변수</span><span class="sxs-lookup"><span data-stu-id="09f1b-112">PARAMETERS</span></span>

### <span data-ttu-id="09f1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f1b-113">-DefaultProfile</span></span>
<span data-ttu-id="09f1b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09f1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09f1b-115">-Id</span><span class="sxs-lookup"><span data-stu-id="09f1b-115">-Id</span></span>
<span data-ttu-id="09f1b-116">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="09f1b-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f1b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="09f1b-117">-Name</span></span>
<span data-ttu-id="09f1b-118">관리 되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="09f1b-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f1b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f1b-119">-ResourceGroupName</span></span>
<span data-ttu-id="09f1b-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="09f1b-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f1b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f1b-121">CommonParameters</span></span>
<span data-ttu-id="09f1b-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09f1b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f1b-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09f1b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f1b-124">입력</span><span class="sxs-lookup"><span data-stu-id="09f1b-124">INPUTS</span></span>

### <span data-ttu-id="09f1b-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="09f1b-125">System.String</span></span>

## <span data-ttu-id="09f1b-126">출력</span><span class="sxs-lookup"><span data-stu-id="09f1b-126">OUTPUTS</span></span>

### <span data-ttu-id="09f1b-127">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="09f1b-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="09f1b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="09f1b-128">NOTES</span></span>

## <span data-ttu-id="09f1b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09f1b-129">RELATED LINKS</span></span>
