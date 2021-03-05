---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 42e7b805e772e42ed395f8893b1140faaab715ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993916"
---
# <span data-ttu-id="ca7a4-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca7a4-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="ca7a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7a4-103">자동 승인을 통해 개인 엔드포인트에 연결할 수 있는 개인 링크 서비스 ID의 배열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca7a4-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="ca7a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca7a4-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca7a4-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca7a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ca7a4-106">**Get-AzAutoApprovedPrivateLinkService는** 자동 승인을 통해 개인 엔드포인트에 연결할 수 있는 개인 링크 서비스 ID의 배열을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7a4-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="ca7a4-107">예제</span><span class="sxs-lookup"><span data-stu-id="ca7a4-107">EXAMPLES</span></span>

### <span data-ttu-id="ca7a4-108">예제</span><span class="sxs-lookup"><span data-stu-id="ca7a4-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="ca7a4-109">이 예제에서는 자동 승인된 개인 엔드포인트에 연결할 수 있는 개인 링크 서비스 ID 배열을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7a4-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="ca7a4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca7a4-110">PARAMETERS</span></span>

### <span data-ttu-id="ca7a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7a4-111">-DefaultProfile</span></span>
<span data-ttu-id="ca7a4-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca7a4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca7a4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="ca7a4-113">-Location</span></span>
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

### <span data-ttu-id="ca7a4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca7a4-114">-ResourceGroupName</span></span>
<span data-ttu-id="ca7a4-115">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7a4-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca7a4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7a4-116">CommonParameters</span></span>
<span data-ttu-id="ca7a4-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7a4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7a4-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca7a4-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7a4-119">입력</span><span class="sxs-lookup"><span data-stu-id="ca7a4-119">INPUTS</span></span>

### <span data-ttu-id="ca7a4-120">없음</span><span class="sxs-lookup"><span data-stu-id="ca7a4-120">None</span></span>

## <span data-ttu-id="ca7a4-121">출력</span><span class="sxs-lookup"><span data-stu-id="ca7a4-121">OUTPUTS</span></span>

### <span data-ttu-id="ca7a4-122">Microsoft.Azure.Commands.Network.Models.PSAutoapprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ca7a4-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="ca7a4-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca7a4-123">NOTES</span></span>

## <span data-ttu-id="ca7a4-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca7a4-124">RELATED LINKS</span></span>
