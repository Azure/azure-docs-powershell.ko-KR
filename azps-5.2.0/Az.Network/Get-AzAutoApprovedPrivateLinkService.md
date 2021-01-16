---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338109"
---
# <span data-ttu-id="f4d1d-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4d1d-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="f4d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d1d-103">자동 승인을 통해 개인 끝점에 연결할 수 있는 개인 링크 서비스 ID의 배열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f4d1d-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="f4d1d-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4d1d-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4d1d-105">설명</span><span class="sxs-lookup"><span data-stu-id="f4d1d-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d1d-106">**Get-AzAutoApprovedPrivateLinkService는** 자동 승인을 통해 개인 끝점에 연결할 수 있는 개인 링크 서비스 ID의 배열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f4d1d-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="f4d1d-107">예제</span><span class="sxs-lookup"><span data-stu-id="f4d1d-107">EXAMPLES</span></span>

### <span data-ttu-id="f4d1d-108">예제</span><span class="sxs-lookup"><span data-stu-id="f4d1d-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="f4d1d-109">이 예제에서는 자동 승인을 통해 개인 끝점에 연결할 수 있는 개인 링크 서비스 ID의 배열을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d1d-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="f4d1d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4d1d-110">PARAMETERS</span></span>

### <span data-ttu-id="f4d1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d1d-111">-DefaultProfile</span></span>
<span data-ttu-id="f4d1d-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d1d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d1d-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f4d1d-113">-Location</span></span>
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

### <span data-ttu-id="f4d1d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d1d-114">-ResourceGroupName</span></span>
<span data-ttu-id="f4d1d-115">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d1d-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f4d1d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d1d-116">CommonParameters</span></span>
<span data-ttu-id="f4d1d-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d1d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d1d-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4d1d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d1d-119">입력</span><span class="sxs-lookup"><span data-stu-id="f4d1d-119">INPUTS</span></span>

### <span data-ttu-id="f4d1d-120">없음</span><span class="sxs-lookup"><span data-stu-id="f4d1d-120">None</span></span>

## <span data-ttu-id="f4d1d-121">출력</span><span class="sxs-lookup"><span data-stu-id="f4d1d-121">OUTPUTS</span></span>

### <span data-ttu-id="f4d1d-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f4d1d-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="f4d1d-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4d1d-123">NOTES</span></span>

## <span data-ttu-id="f4d1d-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4d1d-124">RELATED LINKS</span></span>