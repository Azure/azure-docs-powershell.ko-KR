---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpPrefix.md
ms.openlocfilehash: 2937aafbcffd2444051b9bed0a764cb3aede6c52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001051"
---
# <span data-ttu-id="f5adc-101">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f5adc-101">Set-AzPublicIpPrefix</span></span>

## <span data-ttu-id="f5adc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5adc-102">SYNOPSIS</span></span>
<span data-ttu-id="f5adc-103">기존 PublicIpPrefix에 대한 태그 설정</span><span class="sxs-lookup"><span data-stu-id="f5adc-103">Sets the Tags for an existing PublicIpPrefix</span></span>

## <span data-ttu-id="f5adc-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5adc-104">SYNTAX</span></span>

```
Set-AzPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5adc-105">설명</span><span class="sxs-lookup"><span data-stu-id="f5adc-105">DESCRIPTION</span></span>
<span data-ttu-id="f5adc-106">**Set-AzPublicIpPrefix** cmdlet은 공용 IP 연결에 대한 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f5adc-106">The **Set-AzPublicIpPrefix** cmdlet sets the Tags for a public IP prefix.</span></span>

## <span data-ttu-id="f5adc-107">예제</span><span class="sxs-lookup"><span data-stu-id="f5adc-107">EXAMPLES</span></span>

### <span data-ttu-id="f5adc-108">공용 IP 연결에 대한 태그 설정</span><span class="sxs-lookup"><span data-stu-id="f5adc-108">Set the tags for public ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

<span data-ttu-id="f5adc-109">첫 번째 명령은 기존 공용 IP 프리픽스를, 두 번째 명령은 Tags 속성을 설정하고, 세 번째 명령은 기존 개체를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f5adc-109">The first command gets an existing public IP Prefix, the second command sets the Tags Property and the third command updates the existing object.</span></span>

## <span data-ttu-id="f5adc-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f5adc-110">PARAMETERS</span></span>

### <span data-ttu-id="f5adc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5adc-111">-AsJob</span></span>
<span data-ttu-id="f5adc-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f5adc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5adc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5adc-113">-DefaultProfile</span></span>
<span data-ttu-id="f5adc-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5adc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5adc-115">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f5adc-115">-PublicIpPrefix</span></span>
<span data-ttu-id="f5adc-116">The PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f5adc-116">The PublicIpPrefix</span></span>

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

### <span data-ttu-id="f5adc-117">-확인</span><span class="sxs-lookup"><span data-stu-id="f5adc-117">-Confirm</span></span>
<span data-ttu-id="f5adc-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5adc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5adc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5adc-119">-WhatIf</span></span>
<span data-ttu-id="f5adc-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5adc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5adc-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5adc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5adc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5adc-122">CommonParameters</span></span>
<span data-ttu-id="f5adc-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5adc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5adc-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f5adc-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5adc-125">입력</span><span class="sxs-lookup"><span data-stu-id="f5adc-125">INPUTS</span></span>

### <span data-ttu-id="f5adc-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f5adc-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="f5adc-127">출력</span><span class="sxs-lookup"><span data-stu-id="f5adc-127">OUTPUTS</span></span>

### <span data-ttu-id="f5adc-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f5adc-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="f5adc-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5adc-129">NOTES</span></span>

## <span data-ttu-id="f5adc-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5adc-130">RELATED LINKS</span></span>

[<span data-ttu-id="f5adc-131">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f5adc-131">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="f5adc-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f5adc-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="f5adc-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f5adc-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)
