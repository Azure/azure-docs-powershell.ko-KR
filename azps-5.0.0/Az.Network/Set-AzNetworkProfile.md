---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: edbfdcdfc7e02c8bfdb266e1ec7a6b1308c07fa2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218512"
---
# <span data-ttu-id="dbd3c-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dbd3c-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="dbd3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd3c-103">네트워크 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-103">Updates a network profile.</span></span>

## <span data-ttu-id="dbd3c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbd3c-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbd3c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbd3c-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd3c-106">**Set-AzPublicIpPrefix** cmdlet은 네트워크 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="dbd3c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dbd3c-107">EXAMPLES</span></span>

### <span data-ttu-id="dbd3c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dbd3c-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="dbd3c-109">첫 번째 명령은 기존 네트워크 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="dbd3c-110">두 번째 명령은 태그를 업데이트 하 고 셋째는 네트워크 프로필에 네트워크 인터페이스 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="dbd3c-111">네 번째 명령은 네트워크 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="dbd3c-112">변수</span><span class="sxs-lookup"><span data-stu-id="dbd3c-112">PARAMETERS</span></span>

### <span data-ttu-id="dbd3c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbd3c-113">-AsJob</span></span>
<span data-ttu-id="dbd3c-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dbd3c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbd3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd3c-115">-DefaultProfile</span></span>
<span data-ttu-id="dbd3c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd3c-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dbd3c-117">-NetworkProfile</span></span>
<span data-ttu-id="dbd3c-118">네트워크 프로필</span><span class="sxs-lookup"><span data-stu-id="dbd3c-118">The network profile</span></span>

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

### <span data-ttu-id="dbd3c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="dbd3c-119">-Confirm</span></span>
<span data-ttu-id="dbd3c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbd3c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbd3c-121">-WhatIf</span></span>
<span data-ttu-id="dbd3c-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbd3c-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbd3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd3c-124">CommonParameters</span></span>
<span data-ttu-id="dbd3c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd3c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd3c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd3c-127">입력</span><span class="sxs-lookup"><span data-stu-id="dbd3c-127">INPUTS</span></span>

### <span data-ttu-id="dbd3c-128">Microsoft. 네트워크 모델. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dbd3c-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="dbd3c-129">출력</span><span class="sxs-lookup"><span data-stu-id="dbd3c-129">OUTPUTS</span></span>

### <span data-ttu-id="dbd3c-130">Microsoft. 네트워크 모델. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dbd3c-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="dbd3c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="dbd3c-131">NOTES</span></span>

## <span data-ttu-id="dbd3c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbd3c-132">RELATED LINKS</span></span>

[<span data-ttu-id="dbd3c-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dbd3c-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="dbd3c-134">새로운 AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dbd3c-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="dbd3c-135">제거-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dbd3c-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
