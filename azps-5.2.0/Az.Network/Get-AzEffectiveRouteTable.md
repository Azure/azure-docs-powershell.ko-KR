---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367263"
---
# <span data-ttu-id="3e61d-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="3e61d-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="3e61d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e61d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e61d-103">네트워크 인터페이스의 유효 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e61d-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="3e61d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e61d-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e61d-105">설명</span><span class="sxs-lookup"><span data-stu-id="3e61d-105">DESCRIPTION</span></span>
<span data-ttu-id="3e61d-106">**Get-AzEffectiveRouteTable** cmdlet은 네트워크 인터페이스에 적용되는 유효 경로 테이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3e61d-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="3e61d-107">예제</span><span class="sxs-lookup"><span data-stu-id="3e61d-107">EXAMPLES</span></span>

### <span data-ttu-id="3e61d-108">예제 1: 네트워크 인터페이스에서 유효 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e61d-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="3e61d-109">이 명령은 MyResourceGroup이라는 리소스 그룹의 MyNetworkInterface라는 네트워크 인터페이스와 연결된 유효 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3e61d-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="3e61d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e61d-110">PARAMETERS</span></span>

### <span data-ttu-id="3e61d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e61d-111">-AsJob</span></span>
<span data-ttu-id="3e61d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3e61d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e61d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e61d-113">-DefaultProfile</span></span>
<span data-ttu-id="3e61d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e61d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e61d-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="3e61d-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="3e61d-116">네트워크 인터페이스의 이름을 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="3e61d-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="3e61d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e61d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e61d-118">네트워크 인터페이스의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3e61d-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="3e61d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e61d-119">CommonParameters</span></span>
<span data-ttu-id="3e61d-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e61d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e61d-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e61d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e61d-122">입력</span><span class="sxs-lookup"><span data-stu-id="3e61d-122">INPUTS</span></span>

### <span data-ttu-id="3e61d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3e61d-123">System.String</span></span>

## <span data-ttu-id="3e61d-124">출력</span><span class="sxs-lookup"><span data-stu-id="3e61d-124">OUTPUTS</span></span>

### <span data-ttu-id="3e61d-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="3e61d-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="3e61d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e61d-126">NOTES</span></span>

## <span data-ttu-id="3e61d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e61d-127">RELATED LINKS</span></span>

[<span data-ttu-id="3e61d-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3e61d-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


