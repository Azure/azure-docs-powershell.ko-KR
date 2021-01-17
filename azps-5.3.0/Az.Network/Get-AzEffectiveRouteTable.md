---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380185"
---
# <span data-ttu-id="5f392-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5f392-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="5f392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f392-102">SYNOPSIS</span></span>
<span data-ttu-id="5f392-103">네트워크 인터페이스의 유효 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f392-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="5f392-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f392-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f392-105">설명</span><span class="sxs-lookup"><span data-stu-id="5f392-105">DESCRIPTION</span></span>
<span data-ttu-id="5f392-106">**Get-AzEffectiveRouteTable** cmdlet은 네트워크 인터페이스에 적용되는 유효 경로 테이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5f392-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="5f392-107">예제</span><span class="sxs-lookup"><span data-stu-id="5f392-107">EXAMPLES</span></span>

### <span data-ttu-id="5f392-108">예제 1: 네트워크 인터페이스에서 유효 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f392-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5f392-109">이 명령은 MyResourceGroup이라는 리소스 그룹의 MyNetworkInterface라는 네트워크 인터페이스와 연결된 유효 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5f392-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5f392-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f392-110">PARAMETERS</span></span>

### <span data-ttu-id="5f392-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f392-111">-AsJob</span></span>
<span data-ttu-id="5f392-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5f392-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f392-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f392-113">-DefaultProfile</span></span>
<span data-ttu-id="5f392-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f392-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f392-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5f392-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="5f392-116">네트워크 인터페이스의 이름을 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="5f392-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="5f392-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f392-117">-ResourceGroupName</span></span>
<span data-ttu-id="5f392-118">네트워크 인터페이스의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f392-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="5f392-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f392-119">CommonParameters</span></span>
<span data-ttu-id="5f392-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f392-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f392-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5f392-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f392-122">입력</span><span class="sxs-lookup"><span data-stu-id="5f392-122">INPUTS</span></span>

### <span data-ttu-id="5f392-123">System.String</span><span class="sxs-lookup"><span data-stu-id="5f392-123">System.String</span></span>

## <span data-ttu-id="5f392-124">출력</span><span class="sxs-lookup"><span data-stu-id="5f392-124">OUTPUTS</span></span>

### <span data-ttu-id="5f392-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="5f392-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="5f392-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f392-126">NOTES</span></span>

## <span data-ttu-id="5f392-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f392-127">RELATED LINKS</span></span>

[<span data-ttu-id="5f392-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5f392-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


