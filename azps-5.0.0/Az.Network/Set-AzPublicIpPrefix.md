---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 4244f8c97090009272933d73a64323e4af5dfbbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218807"
---
# <span data-ttu-id="5d39a-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5d39a-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="5d39a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d39a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d39a-103">기존 PublicIpPrefix에 대 한 태그 설정</span><span class="sxs-lookup"><span data-stu-id="5d39a-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="5d39a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d39a-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d39a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5d39a-105">DESCRIPTION</span></span>
<span data-ttu-id="5d39a-106">**AzPublicIpPrefix** cmdlet은 공용 IP 접두사에 대 한 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d39a-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="5d39a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5d39a-107">EXAMPLES</span></span>

### <span data-ttu-id="5d39a-108">공용 ip 접두사에 대 한 태그 설정</span><span class="sxs-lookup"><span data-stu-id="5d39a-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="5d39a-109">첫 번째 명령은 기존 공용 IP 접두사를 가져오고, 두 번째 명령은 Tags 속성을 설정 하 고, 세 번째 명령은 기존 개체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d39a-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="5d39a-110">변수</span><span class="sxs-lookup"><span data-stu-id="5d39a-110">PARAMETERS</span></span>

### <span data-ttu-id="5d39a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d39a-111">-AsJob</span></span>
<span data-ttu-id="5d39a-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5d39a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d39a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d39a-113">-DefaultProfile</span></span>
<span data-ttu-id="5d39a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d39a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d39a-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5d39a-115">-PublicIpPrefix</span></span>
<span data-ttu-id="5d39a-116">PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5d39a-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="5d39a-117">-확인</span><span class="sxs-lookup"><span data-stu-id="5d39a-117">-Confirm</span></span>
<span data-ttu-id="5d39a-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d39a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d39a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d39a-119">-WhatIf</span></span>
<span data-ttu-id="5d39a-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d39a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d39a-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d39a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d39a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d39a-122">CommonParameters</span></span>
<span data-ttu-id="5d39a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d39a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d39a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d39a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d39a-125">입력</span><span class="sxs-lookup"><span data-stu-id="5d39a-125">INPUTS</span></span>

### <span data-ttu-id="5d39a-126">PSPublicIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5d39a-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="5d39a-127">출력</span><span class="sxs-lookup"><span data-stu-id="5d39a-127">OUTPUTS</span></span>

### <span data-ttu-id="5d39a-128">PSPublicIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5d39a-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="5d39a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="5d39a-129">NOTES</span></span>

## <span data-ttu-id="5d39a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d39a-130">RELATED LINKS</span></span>

[<span data-ttu-id="5d39a-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5d39a-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="5d39a-132">새로운 AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5d39a-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="5d39a-133">제거-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="5d39a-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
