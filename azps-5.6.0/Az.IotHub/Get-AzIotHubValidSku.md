---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: b51c41ddd36d19afedd0091be9b0a00bb447faaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964619"
---
# <span data-ttu-id="39dea-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="39dea-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="39dea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39dea-102">SYNOPSIS</span></span>
<span data-ttu-id="39dea-103">이 IotHub로 전환할 수 있는 유효한 모든 스쿠를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39dea-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="39dea-104">구문</span><span class="sxs-lookup"><span data-stu-id="39dea-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39dea-105">설명</span><span class="sxs-lookup"><span data-stu-id="39dea-105">DESCRIPTION</span></span>
<span data-ttu-id="39dea-106">이 IotHub로 전환할 수 있는 유효한 모든 스쿠를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39dea-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="39dea-107">IotHub는 무료 스쿠와 유료 스쿠 간에 전환할 수 없습니다. 그 반대의 경우도 마찬가지입니다.</span><span class="sxs-lookup"><span data-stu-id="39dea-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="39dea-108">이를 달성하려면 iothub를 삭제하고 다시해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39dea-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="39dea-109">예제</span><span class="sxs-lookup"><span data-stu-id="39dea-109">EXAMPLES</span></span>

### <span data-ttu-id="39dea-110">예제 1 유효한 스쿠스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39dea-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="39dea-111">"myiothub"라는 IotHub에 대한 모든 스쿠 목록이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="39dea-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="39dea-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="39dea-112">PARAMETERS</span></span>

### <span data-ttu-id="39dea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39dea-113">-DefaultProfile</span></span>
<span data-ttu-id="39dea-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="39dea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39dea-115">-Name</span><span class="sxs-lookup"><span data-stu-id="39dea-115">-Name</span></span>
<span data-ttu-id="39dea-116">IoT 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39dea-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39dea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39dea-117">-ResourceGroupName</span></span>
<span data-ttu-id="39dea-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="39dea-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39dea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39dea-119">CommonParameters</span></span>
<span data-ttu-id="39dea-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39dea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39dea-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="39dea-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39dea-122">입력</span><span class="sxs-lookup"><span data-stu-id="39dea-122">INPUTS</span></span>

### <span data-ttu-id="39dea-123">System.String</span><span class="sxs-lookup"><span data-stu-id="39dea-123">System.String</span></span>

## <span data-ttu-id="39dea-124">출력</span><span class="sxs-lookup"><span data-stu-id="39dea-124">OUTPUTS</span></span>

### <span data-ttu-id="39dea-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="39dea-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="39dea-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39dea-126">NOTES</span></span>

## <span data-ttu-id="39dea-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39dea-127">RELATED LINKS</span></span>
