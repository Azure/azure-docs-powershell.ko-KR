---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046333"
---
# <span data-ttu-id="e2cb2-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="e2cb2-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="e2cb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="e2cb2-103">네트워크 보안 그룹에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="e2cb2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2cb2-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2cb2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2cb2-105">DESCRIPTION</span></span>
<span data-ttu-id="e2cb2-106">**AzureNetworkSecurityGroupConfig** cmdlet은 네트워크 보안 그룹에 대 한 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="e2cb2-107">*자세한* 매개 변수를 지정 하 여 네트워크 보안 규칙을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="e2cb2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e2cb2-108">EXAMPLES</span></span>

## <span data-ttu-id="e2cb2-109">변수</span><span class="sxs-lookup"><span data-stu-id="e2cb2-109">PARAMETERS</span></span>

### <span data-ttu-id="e2cb2-110">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="e2cb2-110">-Detailed</span></span>
<span data-ttu-id="e2cb2-111">이 cmdlet에 네트워크 보안 규칙이 표시 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-111">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="e2cb2-112">-프로필</span><span class="sxs-lookup"><span data-stu-id="e2cb2-112">-Profile</span></span>
<span data-ttu-id="e2cb2-113">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e2cb2-114">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2cb2-115">-VM</span><span class="sxs-lookup"><span data-stu-id="e2cb2-115">-VM</span></span>
<span data-ttu-id="e2cb2-116">이 cmdlet이 네트워크 보안 그룹의 세부 정보를 가져오는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2cb2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2cb2-117">CommonParameters</span></span>
<span data-ttu-id="e2cb2-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2cb2-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2cb2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2cb2-120">입력</span><span class="sxs-lookup"><span data-stu-id="e2cb2-120">INPUTS</span></span>

## <span data-ttu-id="e2cb2-121">출력</span><span class="sxs-lookup"><span data-stu-id="e2cb2-121">OUTPUTS</span></span>

## <span data-ttu-id="e2cb2-122">상속자</span><span class="sxs-lookup"><span data-stu-id="e2cb2-122">NOTES</span></span>

## <span data-ttu-id="e2cb2-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2cb2-123">RELATED LINKS</span></span>

[<span data-ttu-id="e2cb2-124">새로운 AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2cb2-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="e2cb2-125">제거-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2cb2-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


