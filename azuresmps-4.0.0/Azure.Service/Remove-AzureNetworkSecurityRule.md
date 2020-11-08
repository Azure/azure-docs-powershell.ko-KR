---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045869"
---
# <span data-ttu-id="44abe-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="44abe-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="44abe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44abe-102">SYNOPSIS</span></span>
<span data-ttu-id="44abe-103">네트워크 보안 그룹에서 네트워크 보안 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44abe-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="44abe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44abe-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44abe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44abe-105">DESCRIPTION</span></span>
<span data-ttu-id="44abe-106">**AzureNetworkSecurityRule** cmdlet은 네트워크 보안 그룹에서 Azure 네트워크 보안 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44abe-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="44abe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44abe-107">EXAMPLES</span></span>

## <span data-ttu-id="44abe-108">변수</span><span class="sxs-lookup"><span data-stu-id="44abe-108">PARAMETERS</span></span>

### <span data-ttu-id="44abe-109">-Force</span><span class="sxs-lookup"><span data-stu-id="44abe-109">-Force</span></span>
<span data-ttu-id="44abe-110">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="44abe-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44abe-111">-이름</span><span class="sxs-lookup"><span data-stu-id="44abe-111">-Name</span></span>
<span data-ttu-id="44abe-112">이 cmdlet이 제거 하는 네트워크 보안 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44abe-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="44abe-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="44abe-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="44abe-114">이 cmdlet이 수정 하는 네트워크 보안 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44abe-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="44abe-115">**INetworkSecurityGroup** 개체를 가져오려면 Get-AzureNetworkSecurityGroup cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44abe-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44abe-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="44abe-116">-Profile</span></span>
<span data-ttu-id="44abe-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44abe-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="44abe-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="44abe-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44abe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44abe-119">CommonParameters</span></span>
<span data-ttu-id="44abe-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44abe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44abe-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44abe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44abe-122">입력</span><span class="sxs-lookup"><span data-stu-id="44abe-122">INPUTS</span></span>

## <span data-ttu-id="44abe-123">출력</span><span class="sxs-lookup"><span data-stu-id="44abe-123">OUTPUTS</span></span>

## <span data-ttu-id="44abe-124">상속자</span><span class="sxs-lookup"><span data-stu-id="44abe-124">NOTES</span></span>

## <span data-ttu-id="44abe-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44abe-125">RELATED LINKS</span></span>

[<span data-ttu-id="44abe-126">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="44abe-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


