---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 7050e348530231d9ecc7fbec443f15238f6a41f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711874"
---
# <span data-ttu-id="d7080-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7080-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="d7080-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7080-102">SYNOPSIS</span></span>
<span data-ttu-id="d7080-103">사용자가 New-AzureRmVpnClientConfiguration를 사용 하 여 생성 된 Vpn 프로필 패키지를 쉽게 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d7080-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7080-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7080-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7080-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7080-105">DESCRIPTION</span></span>
<span data-ttu-id="d7080-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="d7080-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d7080-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d7080-107">EXAMPLES</span></span>

### <span data-ttu-id="d7080-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d7080-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="d7080-109">New-AzureRMVpnClientConfiguration 명령을 사용 하 여 이전에 생성 된 VpnClient 프로필을 다운로드할 수 있는 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d7080-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="d7080-110">변수</span><span class="sxs-lookup"><span data-stu-id="d7080-110">PARAMETERS</span></span>

### <span data-ttu-id="d7080-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7080-111">-DefaultProfile</span></span>
<span data-ttu-id="d7080-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7080-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="d7080-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d7080-113">-Name</span></span>
<span data-ttu-id="d7080-114">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7080-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7080-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7080-115">-ResourceGroupName</span></span>
<span data-ttu-id="d7080-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7080-116">The resource group name.</span></span>

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

### <span data-ttu-id="d7080-117">-확인</span><span class="sxs-lookup"><span data-stu-id="d7080-117">-Confirm</span></span>
<span data-ttu-id="d7080-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7080-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7080-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7080-119">-WhatIf</span></span>
<span data-ttu-id="d7080-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d7080-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7080-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7080-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7080-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7080-122">CommonParameters</span></span>
<span data-ttu-id="d7080-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7080-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7080-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7080-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7080-125">입력</span><span class="sxs-lookup"><span data-stu-id="d7080-125">INPUTS</span></span>

### <span data-ttu-id="d7080-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d7080-126">System.String</span></span>

## <span data-ttu-id="d7080-127">출력</span><span class="sxs-lookup"><span data-stu-id="d7080-127">OUTPUTS</span></span>

### <span data-ttu-id="d7080-128">PSVpnProfile에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d7080-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="d7080-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d7080-129">NOTES</span></span>

## <span data-ttu-id="d7080-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7080-130">RELATED LINKS</span></span>

