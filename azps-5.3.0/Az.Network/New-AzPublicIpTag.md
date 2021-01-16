---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 5d7d73b3c7f49babc9e80929dab7b3fa2adad20a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490976"
---
# <span data-ttu-id="d400f-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="d400f-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="d400f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d400f-102">SYNOPSIS</span></span>
<span data-ttu-id="d400f-103">IP 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d400f-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="d400f-104">구문</span><span class="sxs-lookup"><span data-stu-id="d400f-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d400f-105">설명</span><span class="sxs-lookup"><span data-stu-id="d400f-105">DESCRIPTION</span></span>
<span data-ttu-id="d400f-106">**New-AzPublicIpTag** cmdlet은 IP 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d400f-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="d400f-107">예제</span><span class="sxs-lookup"><span data-stu-id="d400f-107">EXAMPLES</span></span>

### <span data-ttu-id="d400f-108">예제 1: 새 IP 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="d400f-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="d400f-109">이 명령은 "FirstPartyUsage"와 같은 태그와 "/Sql"과 같은 태그를 사용하여 새 IP 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d400f-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="d400f-110">할당을 위해 이러한 특정 태그를 사용하여 publicIpAddress를 만들 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d400f-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="d400f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d400f-111">PARAMETERS</span></span>

### <span data-ttu-id="d400f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d400f-112">-DefaultProfile</span></span>
<span data-ttu-id="d400f-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d400f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d400f-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="d400f-114">-IpTagType</span></span>
<span data-ttu-id="d400f-115">IpTag 형식 예제:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="d400f-115">IpTag type Example:FirstPartyUsage</span></span>

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

### <span data-ttu-id="d400f-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="d400f-116">-Tag</span></span>
<span data-ttu-id="d400f-117">IpTag 값 예제:/Sql</span><span class="sxs-lookup"><span data-stu-id="d400f-117">IpTag value Example:/Sql</span></span>

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

### <span data-ttu-id="d400f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d400f-118">-Confirm</span></span>
<span data-ttu-id="d400f-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d400f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d400f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d400f-120">-WhatIf</span></span>
<span data-ttu-id="d400f-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d400f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d400f-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d400f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d400f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d400f-123">CommonParameters</span></span>
<span data-ttu-id="d400f-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d400f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d400f-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d400f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d400f-126">입력</span><span class="sxs-lookup"><span data-stu-id="d400f-126">INPUTS</span></span>

### <span data-ttu-id="d400f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d400f-127">System.String</span></span>

## <span data-ttu-id="d400f-128">출력</span><span class="sxs-lookup"><span data-stu-id="d400f-128">OUTPUTS</span></span>

### <span data-ttu-id="d400f-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="d400f-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="d400f-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d400f-130">NOTES</span></span>

## <span data-ttu-id="d400f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d400f-131">RELATED LINKS</span></span>
