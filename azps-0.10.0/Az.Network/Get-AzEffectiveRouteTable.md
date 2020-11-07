---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 37c9827f2af970c0c376c31f4d67ba7723e02e99
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875602"
---
# <span data-ttu-id="8f1d4-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="8f1d4-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="8f1d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="8f1d4-103">네트워크 인터페이스의 유효한 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="8f1d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f1d4-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f1d4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8f1d4-105">DESCRIPTION</span></span>
<span data-ttu-id="8f1d4-106">**AzEffectiveRouteTable** cmdlet은 네트워크 인터페이스에 적용 되는 유효한 경로 테이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="8f1d4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8f1d4-107">EXAMPLES</span></span>

### <span data-ttu-id="8f1d4-108">예제 1: 네트워크 인터페이스에서 유효한 경로 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="8f1d4-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8f1d4-109">이 명령은 MyResourceGroup 이라는 리소스 그룹의 MyNetworkInterface 이라는 네트워크 인터페이스와 연결 된 유효 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="8f1d4-110">변수</span><span class="sxs-lookup"><span data-stu-id="8f1d4-110">PARAMETERS</span></span>

### <span data-ttu-id="8f1d4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f1d4-111">-AsJob</span></span>
<span data-ttu-id="8f1d4-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8f1d4-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f1d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f1d4-113">-DefaultProfile</span></span>
<span data-ttu-id="8f1d4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f1d4-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="8f1d4-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="8f1d4-116">네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="8f1d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f1d4-118">네트워크 인터페이스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f1d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f1d4-119">CommonParameters</span></span>
<span data-ttu-id="8f1d4-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f1d4-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f1d4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f1d4-122">입력</span><span class="sxs-lookup"><span data-stu-id="8f1d4-122">INPUTS</span></span>

## <span data-ttu-id="8f1d4-123">출력</span><span class="sxs-lookup"><span data-stu-id="8f1d4-123">OUTPUTS</span></span>

### <span data-ttu-id="8f1d4-124">PSEffectiveRoute에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8f1d4-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="8f1d4-125">상속자</span><span class="sxs-lookup"><span data-stu-id="8f1d4-125">NOTES</span></span>

## <span data-ttu-id="8f1d4-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f1d4-126">RELATED LINKS</span></span>

[<span data-ttu-id="8f1d4-127">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f1d4-127">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


