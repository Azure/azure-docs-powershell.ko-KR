---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1836F342-A05C-4402-95F7-833E50A1AB97
online version: ''
schema: 2.0.0
ms.openlocfilehash: c33d48755b731c27f12742e7c21efe39994bc751
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046154"
---
# <span data-ttu-id="b7ad0-101">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7ad0-101">Remove-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="b7ad0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ad0-103">네트워크 보안 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-103">Deletes a network security group.</span></span>

## <span data-ttu-id="b7ad0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7ad0-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroup -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7ad0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b7ad0-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ad0-106">**AzureNetworkSecurityGroup** cmdlet은 구독에서 Azure 네트워크 보안 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-106">The **Remove-AzureNetworkSecurityGroup** cmdlet deletes an Azure network security group from your subscription.</span></span>

## <span data-ttu-id="b7ad0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b7ad0-107">EXAMPLES</span></span>

## <span data-ttu-id="b7ad0-108">변수</span><span class="sxs-lookup"><span data-stu-id="b7ad0-108">PARAMETERS</span></span>

### <span data-ttu-id="b7ad0-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b7ad0-109">-Force</span></span>
<span data-ttu-id="b7ad0-110">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7ad0-111">-이름</span><span class="sxs-lookup"><span data-stu-id="b7ad0-111">-Name</span></span>
<span data-ttu-id="b7ad0-112">이 cmdlet이 삭제 하는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-112">Specifies the name of the network security group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="b7ad0-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7ad0-113">-PassThru</span></span>
<span data-ttu-id="b7ad0-114">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b7ad0-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7ad0-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="b7ad0-116">-Profile</span></span>
<span data-ttu-id="b7ad0-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b7ad0-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b7ad0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ad0-119">CommonParameters</span></span>
<span data-ttu-id="b7ad0-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ad0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ad0-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ad0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ad0-122">입력</span><span class="sxs-lookup"><span data-stu-id="b7ad0-122">INPUTS</span></span>

## <span data-ttu-id="b7ad0-123">출력</span><span class="sxs-lookup"><span data-stu-id="b7ad0-123">OUTPUTS</span></span>

## <span data-ttu-id="b7ad0-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b7ad0-124">NOTES</span></span>

## <span data-ttu-id="b7ad0-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7ad0-125">RELATED LINKS</span></span>

[<span data-ttu-id="b7ad0-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7ad0-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="b7ad0-127">새로운 AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7ad0-127">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)


