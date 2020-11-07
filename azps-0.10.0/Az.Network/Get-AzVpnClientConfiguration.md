---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 63b044c4a9736aca72e9713cd8ec5833e7b056ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875505"
---
# <span data-ttu-id="48c07-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="48c07-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="48c07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48c07-102">SYNOPSIS</span></span>
<span data-ttu-id="48c07-103">사용자가 New-AzVpnClientConfiguration를 사용 하 여 생성 된 Vpn 프로필 패키지를 쉽게 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48c07-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="48c07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48c07-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48c07-105">설명은</span><span class="sxs-lookup"><span data-stu-id="48c07-105">DESCRIPTION</span></span>
<span data-ttu-id="48c07-106">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="48c07-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="48c07-107">예제의</span><span class="sxs-lookup"><span data-stu-id="48c07-107">EXAMPLES</span></span>

### <span data-ttu-id="48c07-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="48c07-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="48c07-109">New-AzVpnClientConfiguration 명령을 사용 하 여 이전에 생성 된 VpnClient 프로필을 다운로드할 수 있는 URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48c07-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="48c07-110">변수</span><span class="sxs-lookup"><span data-stu-id="48c07-110">PARAMETERS</span></span>

### <span data-ttu-id="48c07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c07-111">-DefaultProfile</span></span>
<span data-ttu-id="48c07-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48c07-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c07-113">-이름</span><span class="sxs-lookup"><span data-stu-id="48c07-113">-Name</span></span>
<span data-ttu-id="48c07-114">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48c07-114">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c07-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c07-115">-ResourceGroupName</span></span>
<span data-ttu-id="48c07-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48c07-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c07-117">-확인</span><span class="sxs-lookup"><span data-stu-id="48c07-117">-Confirm</span></span>
<span data-ttu-id="48c07-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="48c07-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c07-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48c07-119">-WhatIf</span></span>
<span data-ttu-id="48c07-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="48c07-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48c07-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48c07-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c07-122">CommonParameters</span></span>
<span data-ttu-id="48c07-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48c07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c07-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c07-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c07-125">입력</span><span class="sxs-lookup"><span data-stu-id="48c07-125">INPUTS</span></span>

### <span data-ttu-id="48c07-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="48c07-126">System.String</span></span>

## <span data-ttu-id="48c07-127">출력</span><span class="sxs-lookup"><span data-stu-id="48c07-127">OUTPUTS</span></span>

### <span data-ttu-id="48c07-128">PSVpnProfile에 대 한.</span><span class="sxs-lookup"><span data-stu-id="48c07-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="48c07-129">상속자</span><span class="sxs-lookup"><span data-stu-id="48c07-129">NOTES</span></span>

## <span data-ttu-id="48c07-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48c07-130">RELATED LINKS</span></span>

