---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 2f46b13570ef1f538658dae6d02000848822c150
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953888"
---
# <span data-ttu-id="bd46b-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="bd46b-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="bd46b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd46b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd46b-103">IP 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd46b-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="bd46b-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd46b-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd46b-105">설명</span><span class="sxs-lookup"><span data-stu-id="bd46b-105">DESCRIPTION</span></span>
<span data-ttu-id="bd46b-106">**New-AzPublicIpTag** cmdlet은 IP 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd46b-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="bd46b-107">예제</span><span class="sxs-lookup"><span data-stu-id="bd46b-107">EXAMPLES</span></span>

### <span data-ttu-id="bd46b-108">예제 1: 새 IP 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="bd46b-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="bd46b-109">이 명령은 "FirstPartyUsage"와 같은 태그와 "/Sql"과 같은 태그를 사용하여 새 IP 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd46b-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="bd46b-110">이 태그는 할당을 위해 이러한 특정 태그를 사용하여 publicIpAddress 만들기에 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd46b-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="bd46b-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bd46b-111">PARAMETERS</span></span>

### <span data-ttu-id="bd46b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd46b-112">-DefaultProfile</span></span>
<span data-ttu-id="bd46b-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd46b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd46b-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="bd46b-114">-IpTagType</span></span>
<span data-ttu-id="bd46b-115">IpTag 형식 예제:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="bd46b-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="bd46b-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd46b-116">-Tag</span></span>
<span data-ttu-id="bd46b-117">IpTag 값 예제:/SQL</span><span class="sxs-lookup"><span data-stu-id="bd46b-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="bd46b-118">-확인</span><span class="sxs-lookup"><span data-stu-id="bd46b-118">-Confirm</span></span>
<span data-ttu-id="bd46b-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd46b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd46b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd46b-120">-WhatIf</span></span>
<span data-ttu-id="bd46b-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bd46b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd46b-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd46b-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd46b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd46b-123">CommonParameters</span></span>
<span data-ttu-id="bd46b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd46b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd46b-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd46b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd46b-126">입력</span><span class="sxs-lookup"><span data-stu-id="bd46b-126">INPUTS</span></span>

### <span data-ttu-id="bd46b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bd46b-127">System.String</span></span>

## <span data-ttu-id="bd46b-128">출력</span><span class="sxs-lookup"><span data-stu-id="bd46b-128">OUTPUTS</span></span>

### <span data-ttu-id="bd46b-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="bd46b-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="bd46b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd46b-130">NOTES</span></span>

## <span data-ttu-id="bd46b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd46b-131">RELATED LINKS</span></span>
