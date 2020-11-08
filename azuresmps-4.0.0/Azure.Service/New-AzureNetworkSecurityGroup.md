---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045910"
---
# <span data-ttu-id="83b10-101">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83b10-101">New-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="83b10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b10-102">SYNOPSIS</span></span>
<span data-ttu-id="83b10-103">Azure 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83b10-103">Creates an Azure network security group.</span></span>

## <span data-ttu-id="83b10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83b10-104">SYNTAX</span></span>

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="83b10-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83b10-105">DESCRIPTION</span></span>
<span data-ttu-id="83b10-106">**AzureNetworkSecurityGroup** cmdlet은 위치에 Azure 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="83b10-106">The **New-AzureNetworkSecurityGroup** cmdlet creates an Azure network security group in a location.</span></span>

## <span data-ttu-id="83b10-107">예제의</span><span class="sxs-lookup"><span data-stu-id="83b10-107">EXAMPLES</span></span>

## <span data-ttu-id="83b10-108">변수</span><span class="sxs-lookup"><span data-stu-id="83b10-108">PARAMETERS</span></span>

### <span data-ttu-id="83b10-109">-레이블</span><span class="sxs-lookup"><span data-stu-id="83b10-109">-Label</span></span>
<span data-ttu-id="83b10-110">새 네트워크 보안 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b10-110">Specifies a description for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b10-111">-위치</span><span class="sxs-lookup"><span data-stu-id="83b10-111">-Location</span></span>
<span data-ttu-id="83b10-112">이 cmdlet이 네트워크 보안 그룹을 만드는 Azure 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b10-112">Specifies the Azure location in which this cmdlet creates a network security group.</span></span>
<span data-ttu-id="83b10-113">유효한 위치를 얻으려면 Get-AzureLocation cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b10-113">To obtain valid locations, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b10-114">-이름</span><span class="sxs-lookup"><span data-stu-id="83b10-114">-Name</span></span>
<span data-ttu-id="83b10-115">새 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b10-115">Specifies a name for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83b10-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="83b10-116">-Profile</span></span>
<span data-ttu-id="83b10-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b10-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="83b10-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="83b10-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83b10-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b10-119">CommonParameters</span></span>
<span data-ttu-id="83b10-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83b10-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b10-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b10-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b10-122">입력</span><span class="sxs-lookup"><span data-stu-id="83b10-122">INPUTS</span></span>

## <span data-ttu-id="83b10-123">출력</span><span class="sxs-lookup"><span data-stu-id="83b10-123">OUTPUTS</span></span>

## <span data-ttu-id="83b10-124">상속자</span><span class="sxs-lookup"><span data-stu-id="83b10-124">NOTES</span></span>

## <span data-ttu-id="83b10-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83b10-125">RELATED LINKS</span></span>

[<span data-ttu-id="83b10-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83b10-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)


