---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216369"
---
# <span data-ttu-id="754be-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="754be-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="754be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="754be-102">SYNOPSIS</span></span>
<span data-ttu-id="754be-103">PeerAsn에 대 한 in 메모리 연락처 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="754be-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="754be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="754be-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="754be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="754be-105">DESCRIPTION</span></span>
<span data-ttu-id="754be-106">메모리 PeerAsn 연락처 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="754be-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="754be-107">예제의</span><span class="sxs-lookup"><span data-stu-id="754be-107">EXAMPLES</span></span>

### <span data-ttu-id="754be-108">연락처 세부 정보를 만들고 PeerAsn에 추가</span><span class="sxs-lookup"><span data-stu-id="754be-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="754be-109">역할 및 전자 메일이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="754be-109">Role and email are required.</span></span> <span data-ttu-id="754be-110">전화는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="754be-110">Phone is optional.</span></span> <span data-ttu-id="754be-111">전화는 +-() 또는 공백을 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="754be-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="754be-112">PeerAsn에는 "Noc" 유형의 연락처 세부 정보가 하나 이상 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="754be-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="754be-113">변수</span><span class="sxs-lookup"><span data-stu-id="754be-113">PARAMETERS</span></span>

### <span data-ttu-id="754be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="754be-114">-DefaultProfile</span></span>
<span data-ttu-id="754be-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="754be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="754be-116">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="754be-116">-Email</span></span>
<span data-ttu-id="754be-117">일반적으로 네트워크 작업 센터에 문제가 arrise 때 연락 하는 데 사용 되는 전자 메일 주소</span><span class="sxs-lookup"><span data-stu-id="754be-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754be-118">-전화</span><span class="sxs-lookup"><span data-stu-id="754be-118">-Phone</span></span>
<span data-ttu-id="754be-119">일반적으로 네트워크 작업 센터에 문제가 arrise 때 사용 하는 전화</span><span class="sxs-lookup"><span data-stu-id="754be-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754be-120">-역할</span><span class="sxs-lookup"><span data-stu-id="754be-120">-Role</span></span>
<span data-ttu-id="754be-121">연락처 정보에 가장 적합 한 역할을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="754be-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="754be-122">NOC Contact가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="754be-122">NOC Contact is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="754be-123">CommonParameters</span></span>
<span data-ttu-id="754be-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="754be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="754be-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="754be-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="754be-126">입력</span><span class="sxs-lookup"><span data-stu-id="754be-126">INPUTS</span></span>

### <span data-ttu-id="754be-127">않아야</span><span class="sxs-lookup"><span data-stu-id="754be-127">None</span></span>

## <span data-ttu-id="754be-128">출력</span><span class="sxs-lookup"><span data-stu-id="754be-128">OUTPUTS</span></span>

### <span data-ttu-id="754be-129">Microsoft. PowerShell. a i m/. i a m a 모델 정보</span><span class="sxs-lookup"><span data-stu-id="754be-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="754be-130">상속자</span><span class="sxs-lookup"><span data-stu-id="754be-130">NOTES</span></span>

## <span data-ttu-id="754be-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="754be-131">RELATED LINKS</span></span>
