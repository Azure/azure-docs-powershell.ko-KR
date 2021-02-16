---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: edbfdcdfc7e02c8bfdb266e1ec7a6b1308c07fa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186844"
---
# <span data-ttu-id="580bd-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="580bd-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="580bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="580bd-102">SYNOPSIS</span></span>
<span data-ttu-id="580bd-103">네트워크 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="580bd-103">Updates a network profile.</span></span>

## <span data-ttu-id="580bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="580bd-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="580bd-105">설명</span><span class="sxs-lookup"><span data-stu-id="580bd-105">DESCRIPTION</span></span>
<span data-ttu-id="580bd-106">**Set-AzPublicIpPrefix** cmdlet은 네트워크 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="580bd-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="580bd-107">예제</span><span class="sxs-lookup"><span data-stu-id="580bd-107">EXAMPLES</span></span>

### <span data-ttu-id="580bd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="580bd-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="580bd-109">첫 번째 명령은 기존 네트워크 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="580bd-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="580bd-110">두 번째 명령은 태그를 업데이트하고 세 번째 명령은 네트워크 프로필에 네트워크 인터페이스 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="580bd-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="580bd-111">네 번째 명령은 네트워크 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="580bd-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="580bd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="580bd-112">PARAMETERS</span></span>

### <span data-ttu-id="580bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="580bd-113">-AsJob</span></span>
<span data-ttu-id="580bd-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="580bd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="580bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580bd-115">-DefaultProfile</span></span>
<span data-ttu-id="580bd-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="580bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="580bd-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="580bd-117">-NetworkProfile</span></span>
<span data-ttu-id="580bd-118">네트워크 프로필</span><span class="sxs-lookup"><span data-stu-id="580bd-118">The network profile</span></span>

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

### <span data-ttu-id="580bd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="580bd-119">-Confirm</span></span>
<span data-ttu-id="580bd-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="580bd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="580bd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="580bd-121">-WhatIf</span></span>
<span data-ttu-id="580bd-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="580bd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="580bd-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="580bd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="580bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580bd-124">CommonParameters</span></span>
<span data-ttu-id="580bd-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="580bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580bd-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="580bd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580bd-127">입력</span><span class="sxs-lookup"><span data-stu-id="580bd-127">INPUTS</span></span>

### <span data-ttu-id="580bd-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="580bd-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="580bd-129">출력</span><span class="sxs-lookup"><span data-stu-id="580bd-129">OUTPUTS</span></span>

### <span data-ttu-id="580bd-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="580bd-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="580bd-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="580bd-131">NOTES</span></span>

## <span data-ttu-id="580bd-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="580bd-132">RELATED LINKS</span></span>

[<span data-ttu-id="580bd-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="580bd-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="580bd-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="580bd-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="580bd-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="580bd-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
