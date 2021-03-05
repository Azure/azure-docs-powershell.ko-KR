---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: 978c513646c08577f4fa15b8a0e460320878c7c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989450"
---
# <span data-ttu-id="13583-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="13583-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="13583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13583-102">SYNOPSIS</span></span>
<span data-ttu-id="13583-103">PeerAsn에 대한 메모리 내 연락처 세부 정보를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13583-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="13583-104">구문</span><span class="sxs-lookup"><span data-stu-id="13583-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13583-105">설명</span><span class="sxs-lookup"><span data-stu-id="13583-105">DESCRIPTION</span></span>
<span data-ttu-id="13583-106">메모리 내 PeerAsn 연락처 세부 정보를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13583-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="13583-107">예제</span><span class="sxs-lookup"><span data-stu-id="13583-107">EXAMPLES</span></span>

### <span data-ttu-id="13583-108">연락처 세부 정보 만들기 및 PeerAsn에 추가</span><span class="sxs-lookup"><span data-stu-id="13583-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="13583-109">역할 및 전자 메일이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="13583-109">Role and email are required.</span></span> <span data-ttu-id="13583-110">전화는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="13583-110">Phone is optional.</span></span> <span data-ttu-id="13583-111">전화는 +-() 또는 공백을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13583-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="13583-112">PeerAsn은 "Noc" 형식의 하나 이상의 연락처 세부 정보를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13583-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="13583-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="13583-113">PARAMETERS</span></span>

### <span data-ttu-id="13583-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13583-114">-DefaultProfile</span></span>
<span data-ttu-id="13583-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13583-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13583-116">-email</span><span class="sxs-lookup"><span data-stu-id="13583-116">-Email</span></span>
<span data-ttu-id="13583-117">일반적으로 네트워크 작업 센터에서 문제가 해결되는 경우 연락하는 데 사용되는 전자 메일 주소</span><span class="sxs-lookup"><span data-stu-id="13583-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="13583-118">-Phone</span><span class="sxs-lookup"><span data-stu-id="13583-118">-Phone</span></span>
<span data-ttu-id="13583-119">일반적으로 네트워크 작업 센터에서 문제가 해결되는 경우 연락하는 데 사용되는 전화</span><span class="sxs-lookup"><span data-stu-id="13583-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="13583-120">-역할</span><span class="sxs-lookup"><span data-stu-id="13583-120">-Role</span></span>
<span data-ttu-id="13583-121">연락처 정보에 가장 적합한 역할을 선택하세요.</span><span class="sxs-lookup"><span data-stu-id="13583-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="13583-122">NOC 연락처가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="13583-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="13583-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13583-123">CommonParameters</span></span>
<span data-ttu-id="13583-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13583-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13583-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13583-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13583-126">입력</span><span class="sxs-lookup"><span data-stu-id="13583-126">INPUTS</span></span>

### <span data-ttu-id="13583-127">없음</span><span class="sxs-lookup"><span data-stu-id="13583-127">None</span></span>

## <span data-ttu-id="13583-128">출력</span><span class="sxs-lookup"><span data-stu-id="13583-128">OUTPUTS</span></span>

### <span data-ttu-id="13583-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="13583-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="13583-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13583-130">NOTES</span></span>

## <span data-ttu-id="13583-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13583-131">RELATED LINKS</span></span>
