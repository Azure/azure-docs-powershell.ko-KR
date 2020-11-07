---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: 34db847ba7a4051efab32a62c667d3d79ad4ac30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698210"
---
# <span data-ttu-id="790d9-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="790d9-101">Get-AzAks</span></span>

## <span data-ttu-id="790d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="790d9-102">SYNOPSIS</span></span>
<span data-ttu-id="790d9-103">Kubernetes 관리 되는 클러스터 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d9-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="790d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="790d9-104">SYNTAX</span></span>

### <span data-ttu-id="790d9-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="790d9-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="790d9-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="790d9-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="790d9-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="790d9-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="790d9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="790d9-108">DESCRIPTION</span></span>
<span data-ttu-id="790d9-109">Kubernetes 관리 되는 클러스터 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d9-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="790d9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="790d9-110">EXAMPLES</span></span>

### <span data-ttu-id="790d9-111">모든 Kubernetes 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="790d9-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="790d9-112">변수</span><span class="sxs-lookup"><span data-stu-id="790d9-112">PARAMETERS</span></span>

### <span data-ttu-id="790d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790d9-113">-DefaultProfile</span></span>
<span data-ttu-id="790d9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="790d9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="790d9-115">-Id</span><span class="sxs-lookup"><span data-stu-id="790d9-115">-Id</span></span>
<span data-ttu-id="790d9-116">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="790d9-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="790d9-117">-이름</span><span class="sxs-lookup"><span data-stu-id="790d9-117">-Name</span></span>
<span data-ttu-id="790d9-118">관리 되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="790d9-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="790d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="790d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="790d9-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="790d9-120">Resource group name</span></span>

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

### <span data-ttu-id="790d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790d9-121">CommonParameters</span></span>
<span data-ttu-id="790d9-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="790d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790d9-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="790d9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790d9-124">입력</span><span class="sxs-lookup"><span data-stu-id="790d9-124">INPUTS</span></span>

### <span data-ttu-id="790d9-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="790d9-125">System.String</span></span>

## <span data-ttu-id="790d9-126">출력</span><span class="sxs-lookup"><span data-stu-id="790d9-126">OUTPUTS</span></span>

### <span data-ttu-id="790d9-127">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="790d9-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="790d9-128">상속자</span><span class="sxs-lookup"><span data-stu-id="790d9-128">NOTES</span></span>

## <span data-ttu-id="790d9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="790d9-129">RELATED LINKS</span></span>
