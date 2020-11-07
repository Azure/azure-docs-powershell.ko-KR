---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 2b1e781a65eaa6a43c4f8571caf1850f0b04d6cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711772"
---
# <span data-ttu-id="e798a-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e798a-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="e798a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e798a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e798a-103">구문과</span><span class="sxs-lookup"><span data-stu-id="e798a-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e798a-104">설명은</span><span class="sxs-lookup"><span data-stu-id="e798a-104">DESCRIPTION</span></span>

## <span data-ttu-id="e798a-105">예제의</span><span class="sxs-lookup"><span data-stu-id="e798a-105">EXAMPLES</span></span>

### <span data-ttu-id="e798a-106">예제 1: 가상 네트워크 피어 링 제거</span><span class="sxs-lookup"><span data-stu-id="e798a-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e798a-107">변수</span><span class="sxs-lookup"><span data-stu-id="e798a-107">PARAMETERS</span></span>

### <span data-ttu-id="e798a-108">-Force</span><span class="sxs-lookup"><span data-stu-id="e798a-108">-Force</span></span>
<span data-ttu-id="e798a-109">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-109">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e798a-110">-이름</span><span class="sxs-lookup"><span data-stu-id="e798a-110">-Name</span></span>
<span data-ttu-id="e798a-111">가상 네트워크 피어 링 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-111">The virtual network peering name.</span></span>

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

### <span data-ttu-id="e798a-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e798a-112">-PassThru</span></span>
<span data-ttu-id="e798a-113">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e798a-114">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e798a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e798a-115">-ResourceGroupName</span></span>
<span data-ttu-id="e798a-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e798a-116">The resource group name</span></span>

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

### <span data-ttu-id="e798a-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e798a-117">-VirtualNetworkName</span></span>
<span data-ttu-id="e798a-118">가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-118">The virtual network name.</span></span>

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

### <span data-ttu-id="e798a-119">-확인</span><span class="sxs-lookup"><span data-stu-id="e798a-119">-Confirm</span></span>
<span data-ttu-id="e798a-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e798a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e798a-121">-WhatIf</span></span>
<span data-ttu-id="e798a-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e798a-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e798a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e798a-124">-DefaultProfile</span></span>
<span data-ttu-id="e798a-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e798a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e798a-126">CommonParameters</span></span>
<span data-ttu-id="e798a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e798a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e798a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e798a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e798a-129">입력</span><span class="sxs-lookup"><span data-stu-id="e798a-129">INPUTS</span></span>

## <span data-ttu-id="e798a-130">출력</span><span class="sxs-lookup"><span data-stu-id="e798a-130">OUTPUTS</span></span>

## <span data-ttu-id="e798a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e798a-131">NOTES</span></span>

## <span data-ttu-id="e798a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e798a-132">RELATED LINKS</span></span>

