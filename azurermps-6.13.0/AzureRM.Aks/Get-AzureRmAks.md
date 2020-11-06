---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: d30d9858a3050864f5cc86601adf6b598be8c54d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533503"
---
# <span data-ttu-id="5a7a2-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="5a7a2-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="5a7a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7a2-103">Kubernetes 관리 되는 클러스터 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a2-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a7a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a7a2-104">SYNTAX</span></span>

### <span data-ttu-id="5a7a2-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5a7a2-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a7a2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a7a2-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a7a2-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a7a2-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a7a2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5a7a2-108">DESCRIPTION</span></span>
<span data-ttu-id="5a7a2-109">Kubernetes 관리 되는 클러스터 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a2-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="5a7a2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5a7a2-110">EXAMPLES</span></span>

### <span data-ttu-id="5a7a2-111">모든 Kubernetes 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="5a7a2-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="5a7a2-112">변수</span><span class="sxs-lookup"><span data-stu-id="5a7a2-112">PARAMETERS</span></span>

### <span data-ttu-id="5a7a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7a2-113">-DefaultProfile</span></span>
<span data-ttu-id="5a7a2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7a2-115">-Id</span><span class="sxs-lookup"><span data-stu-id="5a7a2-115">-Id</span></span>
<span data-ttu-id="5a7a2-116">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a2-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5a7a2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5a7a2-117">-Name</span></span>
<span data-ttu-id="5a7a2-118">관리 되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="5a7a2-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5a7a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a7a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="5a7a2-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5a7a2-120">Resource group name</span></span>

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

### <span data-ttu-id="5a7a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7a2-121">CommonParameters</span></span>
<span data-ttu-id="5a7a2-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a7a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7a2-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a7a2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7a2-124">입력</span><span class="sxs-lookup"><span data-stu-id="5a7a2-124">INPUTS</span></span>

### <span data-ttu-id="5a7a2-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a7a2-125">System.String</span></span>

## <span data-ttu-id="5a7a2-126">출력</span><span class="sxs-lookup"><span data-stu-id="5a7a2-126">OUTPUTS</span></span>

### <span data-ttu-id="5a7a2-127">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="5a7a2-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="5a7a2-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5a7a2-128">NOTES</span></span>

## <span data-ttu-id="5a7a2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a7a2-129">RELATED LINKS</span></span>
