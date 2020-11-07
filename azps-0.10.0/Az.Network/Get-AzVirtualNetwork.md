---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875523"
---
# <span data-ttu-id="02505-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02505-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="02505-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02505-102">SYNOPSIS</span></span>
<span data-ttu-id="02505-103">리소스 그룹의 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02505-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="02505-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02505-104">SYNTAX</span></span>

### <span data-ttu-id="02505-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="02505-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02505-106">확장</span><span class="sxs-lookup"><span data-stu-id="02505-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02505-107">설명은</span><span class="sxs-lookup"><span data-stu-id="02505-107">DESCRIPTION</span></span>
<span data-ttu-id="02505-108">**AzVirtualNetwork** cmdlet은 하나 이상의 가상 네트워크 n 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02505-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="02505-109">예제의</span><span class="sxs-lookup"><span data-stu-id="02505-109">EXAMPLES</span></span>

### <span data-ttu-id="02505-110">1: 가상 네트워크 검색</span><span class="sxs-lookup"><span data-stu-id="02505-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="02505-111">이 명령은 리소스 그룹 TestResourceGroup에서 MyVirtualNetwork 이라는 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="02505-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="02505-112">변수</span><span class="sxs-lookup"><span data-stu-id="02505-112">PARAMETERS</span></span>

### <span data-ttu-id="02505-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02505-113">-DefaultProfile</span></span>
<span data-ttu-id="02505-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02505-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02505-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="02505-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02505-116">-이름</span><span class="sxs-lookup"><span data-stu-id="02505-116">-Name</span></span>
<span data-ttu-id="02505-117">이 cmdlet이 가져오는 가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02505-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02505-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02505-118">-ResourceGroupName</span></span>
<span data-ttu-id="02505-119">가상 네트워크가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02505-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02505-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02505-120">CommonParameters</span></span>
<span data-ttu-id="02505-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02505-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02505-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02505-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02505-123">입력</span><span class="sxs-lookup"><span data-stu-id="02505-123">INPUTS</span></span>

## <span data-ttu-id="02505-124">출력</span><span class="sxs-lookup"><span data-stu-id="02505-124">OUTPUTS</span></span>

### <span data-ttu-id="02505-125">PSVirtualNetwork에 대 한.</span><span class="sxs-lookup"><span data-stu-id="02505-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="02505-126">상속자</span><span class="sxs-lookup"><span data-stu-id="02505-126">NOTES</span></span>

## <span data-ttu-id="02505-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02505-127">RELATED LINKS</span></span>

[<span data-ttu-id="02505-128">새로운 AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02505-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="02505-129">제거-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02505-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="02505-130">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02505-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


