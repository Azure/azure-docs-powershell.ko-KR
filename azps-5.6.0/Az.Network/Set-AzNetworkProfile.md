---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: 5cb8c8f93b491476e01d5ae54cf2db93ac4a848a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003323"
---
# <span data-ttu-id="33d8c-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d8c-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="33d8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="33d8c-103">네트워크 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-103">Updates a network profile.</span></span>

## <span data-ttu-id="33d8c-104">구문</span><span class="sxs-lookup"><span data-stu-id="33d8c-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d8c-105">설명</span><span class="sxs-lookup"><span data-stu-id="33d8c-105">DESCRIPTION</span></span>
<span data-ttu-id="33d8c-106">**Set-AzPublicIpPrefix** cmdlet은 네트워크 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="33d8c-107">예제</span><span class="sxs-lookup"><span data-stu-id="33d8c-107">EXAMPLES</span></span>

### <span data-ttu-id="33d8c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="33d8c-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="33d8c-109">첫 번째 명령은 기존 네트워크 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="33d8c-110">두 번째 명령은 태그를 업데이트하고 세 번째 명령은 네트워크 프로필에 네트워크 인터페이스 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="33d8c-111">네 번째 명령은 네트워크 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="33d8c-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="33d8c-112">PARAMETERS</span></span>

### <span data-ttu-id="33d8c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33d8c-113">-AsJob</span></span>
<span data-ttu-id="33d8c-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="33d8c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33d8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d8c-115">-DefaultProfile</span></span>
<span data-ttu-id="33d8c-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d8c-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d8c-117">-NetworkProfile</span></span>
<span data-ttu-id="33d8c-118">네트워크 프로필</span><span class="sxs-lookup"><span data-stu-id="33d8c-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33d8c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="33d8c-119">-Confirm</span></span>
<span data-ttu-id="33d8c-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d8c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d8c-121">-WhatIf</span></span>
<span data-ttu-id="33d8c-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33d8c-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33d8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d8c-124">CommonParameters</span></span>
<span data-ttu-id="33d8c-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33d8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d8c-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="33d8c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d8c-127">입력</span><span class="sxs-lookup"><span data-stu-id="33d8c-127">INPUTS</span></span>

### <span data-ttu-id="33d8c-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d8c-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="33d8c-129">출력</span><span class="sxs-lookup"><span data-stu-id="33d8c-129">OUTPUTS</span></span>

### <span data-ttu-id="33d8c-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d8c-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="33d8c-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33d8c-131">NOTES</span></span>

## <span data-ttu-id="33d8c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33d8c-132">RELATED LINKS</span></span>

[<span data-ttu-id="33d8c-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d8c-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="33d8c-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d8c-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="33d8c-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33d8c-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
