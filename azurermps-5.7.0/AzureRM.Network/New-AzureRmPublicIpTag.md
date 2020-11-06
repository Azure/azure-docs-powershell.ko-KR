---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 56352ff165d2e7dcbf5386e713028fae5c991d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535956"
---
# <span data-ttu-id="562d3-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="562d3-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="562d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="562d3-102">SYNOPSIS</span></span>
<span data-ttu-id="562d3-103">IP 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="562d3-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="562d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="562d3-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="562d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="562d3-105">DESCRIPTION</span></span>
<span data-ttu-id="562d3-106">**AzureRmPublicIpTag** CMDLET은 IP 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="562d3-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="562d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="562d3-107">EXAMPLES</span></span>

### <span data-ttu-id="562d3-108">1: 새 IP 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="562d3-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="562d3-109">이 명령은 "FirstPartyUsage"와 같은 Tagtype와 "/Sql" 태그가 지정 된 새 IP 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="562d3-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="562d3-110">이러한 특정 태그를 사용 하 여 배정에 대 한 publicIpAddress 만들기에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="562d3-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="562d3-111">변수</span><span class="sxs-lookup"><span data-stu-id="562d3-111">PARAMETERS</span></span>

### <span data-ttu-id="562d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="562d3-112">-DefaultProfile</span></span>
<span data-ttu-id="562d3-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="562d3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="562d3-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="562d3-114">-IpTagType</span></span>
<span data-ttu-id="562d3-115">IpTag 형식 예: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="562d3-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="562d3-116">태그</span><span class="sxs-lookup"><span data-stu-id="562d3-116">-Tag</span></span>
<span data-ttu-id="562d3-117">IpTag 값 예:/Sql</span><span class="sxs-lookup"><span data-stu-id="562d3-117">IpTag value Example:/Sql</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="562d3-118">-확인</span><span class="sxs-lookup"><span data-stu-id="562d3-118">-Confirm</span></span>
<span data-ttu-id="562d3-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="562d3-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="562d3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="562d3-120">-WhatIf</span></span>
<span data-ttu-id="562d3-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="562d3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="562d3-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="562d3-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="562d3-123">입력</span><span class="sxs-lookup"><span data-stu-id="562d3-123">INPUTS</span></span>

### <span data-ttu-id="562d3-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="562d3-124">System.String</span></span>


## <span data-ttu-id="562d3-125">출력</span><span class="sxs-lookup"><span data-stu-id="562d3-125">OUTPUTS</span></span>

### <span data-ttu-id="562d3-126">PSPublicIpTag에 대 한.</span><span class="sxs-lookup"><span data-stu-id="562d3-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>


## <span data-ttu-id="562d3-127">상속자</span><span class="sxs-lookup"><span data-stu-id="562d3-127">NOTES</span></span>

## <span data-ttu-id="562d3-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="562d3-128">RELATED LINKS</span></span>

