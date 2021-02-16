---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191964"
---
# <span data-ttu-id="36154-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="36154-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="36154-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36154-102">SYNOPSIS</span></span>
<span data-ttu-id="36154-103">네트워크 인터페이스의 유효 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36154-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="36154-104">구문</span><span class="sxs-lookup"><span data-stu-id="36154-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36154-105">설명</span><span class="sxs-lookup"><span data-stu-id="36154-105">DESCRIPTION</span></span>
<span data-ttu-id="36154-106">**Get-AzEffectiveRouteTable** cmdlet은 네트워크 인터페이스에 적용되는 유효 경로 테이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="36154-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="36154-107">예제</span><span class="sxs-lookup"><span data-stu-id="36154-107">EXAMPLES</span></span>

### <span data-ttu-id="36154-108">예제 1: 네트워크 인터페이스에서 유효 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36154-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="36154-109">이 명령은 MyResourceGroup이라는 리소스 그룹의 MyNetworkInterface라는 네트워크 인터페이스와 연결된 유효 경로 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36154-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="36154-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36154-110">PARAMETERS</span></span>

### <span data-ttu-id="36154-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36154-111">-AsJob</span></span>
<span data-ttu-id="36154-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="36154-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36154-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36154-113">-DefaultProfile</span></span>
<span data-ttu-id="36154-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36154-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36154-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="36154-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="36154-116">네트워크 인터페이스의 이름을 지정했습니다.</span><span class="sxs-lookup"><span data-stu-id="36154-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="36154-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36154-117">-ResourceGroupName</span></span>
<span data-ttu-id="36154-118">네트워크 인터페이스의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36154-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="36154-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36154-119">CommonParameters</span></span>
<span data-ttu-id="36154-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36154-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36154-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36154-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36154-122">입력</span><span class="sxs-lookup"><span data-stu-id="36154-122">INPUTS</span></span>

### <span data-ttu-id="36154-123">System.String</span><span class="sxs-lookup"><span data-stu-id="36154-123">System.String</span></span>

## <span data-ttu-id="36154-124">출력</span><span class="sxs-lookup"><span data-stu-id="36154-124">OUTPUTS</span></span>

### <span data-ttu-id="36154-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="36154-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="36154-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36154-126">NOTES</span></span>

## <span data-ttu-id="36154-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36154-127">RELATED LINKS</span></span>

[<span data-ttu-id="36154-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="36154-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


