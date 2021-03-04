---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 7a950bc3b375ea9d86ef71eda120ac1d92fbd8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990346"
---
# <span data-ttu-id="ed335-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ed335-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="ed335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed335-102">SYNOPSIS</span></span>
<span data-ttu-id="ed335-103">Azure 컨테이너 레지스트리의 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ed335-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ed335-104">구문</span><span class="sxs-lookup"><span data-stu-id="ed335-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed335-105">설명</span><span class="sxs-lookup"><span data-stu-id="ed335-105">DESCRIPTION</span></span>
<span data-ttu-id="ed335-106">Azure 컨테이너 레지스트리의 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ed335-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ed335-107">예제</span><span class="sxs-lookup"><span data-stu-id="ed335-107">EXAMPLES</span></span>

### <span data-ttu-id="ed335-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed335-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="ed335-109">Azure 컨테이너 레지스트리의 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ed335-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="ed335-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ed335-110">PARAMETERS</span></span>

### <span data-ttu-id="ed335-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed335-111">-DefaultProfile</span></span>
<span data-ttu-id="ed335-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed335-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed335-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ed335-113">-Name</span></span>
<span data-ttu-id="ed335-114">대상 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed335-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed335-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed335-115">-ResourceGroupName</span></span>
<span data-ttu-id="ed335-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ed335-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed335-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed335-117">CommonParameters</span></span>
<span data-ttu-id="ed335-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ed335-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed335-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed335-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed335-120">입력</span><span class="sxs-lookup"><span data-stu-id="ed335-120">INPUTS</span></span>

### <span data-ttu-id="ed335-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ed335-121">System.String</span></span>

## <span data-ttu-id="ed335-122">출력</span><span class="sxs-lookup"><span data-stu-id="ed335-122">OUTPUTS</span></span>

### <span data-ttu-id="ed335-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="ed335-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="ed335-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ed335-124">NOTES</span></span>

## <span data-ttu-id="ed335-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed335-125">RELATED LINKS</span></span>
