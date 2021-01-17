---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336086"
---
# <span data-ttu-id="6beab-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="6beab-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="6beab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6beab-102">SYNOPSIS</span></span>
<span data-ttu-id="6beab-103">PeerAsn에 대한 메모리 내 연락처 세부 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6beab-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="6beab-104">구문</span><span class="sxs-lookup"><span data-stu-id="6beab-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6beab-105">설명</span><span class="sxs-lookup"><span data-stu-id="6beab-105">DESCRIPTION</span></span>
<span data-ttu-id="6beab-106">메모리 내 PeerAsn 연락처 세부 정보를 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="6beab-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="6beab-107">예제</span><span class="sxs-lookup"><span data-stu-id="6beab-107">EXAMPLES</span></span>

### <span data-ttu-id="6beab-108">연락처 세부 정보를 만들고 PeerAsn에 추가</span><span class="sxs-lookup"><span data-stu-id="6beab-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="6beab-109">역할 및 전자 메일이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="6beab-109">Role and email are required.</span></span> <span data-ttu-id="6beab-110">전화는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6beab-110">Phone is optional.</span></span> <span data-ttu-id="6beab-111">휴대폰은 +-() 또는 공백을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6beab-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="6beab-112">PeerAsn은 "Noc" 형식의 연락처 세부 정보를 하나 이상 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6beab-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="6beab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6beab-113">PARAMETERS</span></span>

### <span data-ttu-id="6beab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6beab-114">-DefaultProfile</span></span>
<span data-ttu-id="6beab-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6beab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6beab-116">-Email</span><span class="sxs-lookup"><span data-stu-id="6beab-116">-Email</span></span>
<span data-ttu-id="6beab-117">일반적으로 네트워크 운영 센터에서 문제가 해결되는 경우 연락하는 데 사용되는 전자 메일 주소</span><span class="sxs-lookup"><span data-stu-id="6beab-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="6beab-118">-Phone</span><span class="sxs-lookup"><span data-stu-id="6beab-118">-Phone</span></span>
<span data-ttu-id="6beab-119">일반적으로 네트워크 운영 센터에서 문제가 있는 경우 연락하는 데 사용되는 전화</span><span class="sxs-lookup"><span data-stu-id="6beab-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="6beab-120">-Role</span><span class="sxs-lookup"><span data-stu-id="6beab-120">-Role</span></span>
<span data-ttu-id="6beab-121">연락처 정보에 가장 적합한 역할을 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="6beab-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="6beab-122">NOC 연락처가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="6beab-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="6beab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6beab-123">CommonParameters</span></span>
<span data-ttu-id="6beab-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6beab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6beab-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6beab-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6beab-126">입력</span><span class="sxs-lookup"><span data-stu-id="6beab-126">INPUTS</span></span>

### <span data-ttu-id="6beab-127">없음</span><span class="sxs-lookup"><span data-stu-id="6beab-127">None</span></span>

## <span data-ttu-id="6beab-128">출력</span><span class="sxs-lookup"><span data-stu-id="6beab-128">OUTPUTS</span></span>

### <span data-ttu-id="6beab-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="6beab-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="6beab-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6beab-130">NOTES</span></span>

## <span data-ttu-id="6beab-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6beab-131">RELATED LINKS</span></span>
