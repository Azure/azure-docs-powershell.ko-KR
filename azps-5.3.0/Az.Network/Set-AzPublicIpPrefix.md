---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496475"
---
# <span data-ttu-id="c5082-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5082-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="c5082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5082-102">SYNOPSIS</span></span>
<span data-ttu-id="c5082-103">기존 PublicIpPrefix에 대한 태그를 설정</span><span class="sxs-lookup"><span data-stu-id="c5082-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="c5082-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5082-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5082-105">설명</span><span class="sxs-lookup"><span data-stu-id="c5082-105">DESCRIPTION</span></span>
<span data-ttu-id="c5082-106">**Set-AzPublicIpPrefix** cmdlet은 공용 IP 주소에 대한 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5082-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="c5082-107">예제</span><span class="sxs-lookup"><span data-stu-id="c5082-107">EXAMPLES</span></span>

### <span data-ttu-id="c5082-108">공용 IP 주소에 대한 태그 설정</span><span class="sxs-lookup"><span data-stu-id="c5082-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="c5082-109">첫 번째 명령은 기존 공용 IP Prefix를, 두 번째 명령은 Tags 속성을 설정하고, 세 번째 명령은 기존 개체를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c5082-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="c5082-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5082-110">PARAMETERS</span></span>

### <span data-ttu-id="c5082-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5082-111">-AsJob</span></span>
<span data-ttu-id="c5082-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c5082-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5082-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5082-113">-DefaultProfile</span></span>
<span data-ttu-id="c5082-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5082-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5082-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5082-115">-PublicIpPrefix</span></span>
<span data-ttu-id="c5082-116">The PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5082-116">The PublicIpPrefix</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5082-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5082-117">-Confirm</span></span>
<span data-ttu-id="c5082-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5082-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5082-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5082-119">-WhatIf</span></span>
<span data-ttu-id="c5082-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c5082-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5082-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5082-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5082-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5082-122">CommonParameters</span></span>
<span data-ttu-id="c5082-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5082-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5082-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c5082-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5082-125">입력</span><span class="sxs-lookup"><span data-stu-id="c5082-125">INPUTS</span></span>

### <span data-ttu-id="c5082-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5082-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="c5082-127">출력</span><span class="sxs-lookup"><span data-stu-id="c5082-127">OUTPUTS</span></span>

### <span data-ttu-id="c5082-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5082-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="c5082-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5082-129">NOTES</span></span>

## <span data-ttu-id="c5082-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5082-130">RELATED LINKS</span></span>

[<span data-ttu-id="c5082-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5082-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="c5082-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5082-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="c5082-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5082-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
