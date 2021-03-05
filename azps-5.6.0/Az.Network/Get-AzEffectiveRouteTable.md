---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 28ec38b9f2dfbb658203aa46fe0d8225aca08a5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967915"
---
# <span data-ttu-id="dc88c-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc88c-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="dc88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc88c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc88c-103">네트워크 인터페이스의 효과적인 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc88c-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="dc88c-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc88c-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc88c-105">설명</span><span class="sxs-lookup"><span data-stu-id="dc88c-105">DESCRIPTION</span></span>
<span data-ttu-id="dc88c-106">**Get-AzEffectiveRouteTable** cmdlet은 네트워크 인터페이스에 적용되는 효과적인 경로 테이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88c-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="dc88c-107">예제</span><span class="sxs-lookup"><span data-stu-id="dc88c-107">EXAMPLES</span></span>

### <span data-ttu-id="dc88c-108">예제 1: 네트워크 인터페이스에서 효과적인 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc88c-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="dc88c-109">이 명령은 MyResourceGroup이라는 리소스 그룹의 MyNetworkInterface라는 네트워크 인터페이스와 연결된 효과적인 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc88c-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="dc88c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dc88c-110">PARAMETERS</span></span>

### <span data-ttu-id="dc88c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc88c-111">-AsJob</span></span>
<span data-ttu-id="dc88c-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dc88c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc88c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc88c-113">-DefaultProfile</span></span>
<span data-ttu-id="dc88c-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc88c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc88c-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="dc88c-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="dc88c-116">네트워크 인터페이스의 이름을 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="dc88c-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="dc88c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc88c-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc88c-118">네트워크 인터페이스의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88c-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="dc88c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc88c-119">CommonParameters</span></span>
<span data-ttu-id="dc88c-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc88c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc88c-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc88c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc88c-122">입력</span><span class="sxs-lookup"><span data-stu-id="dc88c-122">INPUTS</span></span>

### <span data-ttu-id="dc88c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="dc88c-123">System.String</span></span>

## <span data-ttu-id="dc88c-124">출력</span><span class="sxs-lookup"><span data-stu-id="dc88c-124">OUTPUTS</span></span>

### <span data-ttu-id="dc88c-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="dc88c-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="dc88c-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc88c-126">NOTES</span></span>

## <span data-ttu-id="dc88c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc88c-127">RELATED LINKS</span></span>

[<span data-ttu-id="dc88c-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dc88c-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


