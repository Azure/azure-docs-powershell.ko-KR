---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046334"
---
# <span data-ttu-id="78470-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78470-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="78470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78470-102">SYNOPSIS</span></span>
<span data-ttu-id="78470-103">네트워크 보안 그룹에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78470-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="78470-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78470-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="78470-105">설명은</span><span class="sxs-lookup"><span data-stu-id="78470-105">DESCRIPTION</span></span>
<span data-ttu-id="78470-106">**AzureNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹에 대 한 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78470-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="78470-107">*자세한* 매개 변수를 지정 하 여 네트워크 보안 규칙을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78470-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="78470-108">예제의</span><span class="sxs-lookup"><span data-stu-id="78470-108">EXAMPLES</span></span>

## <span data-ttu-id="78470-109">변수</span><span class="sxs-lookup"><span data-stu-id="78470-109">PARAMETERS</span></span>

### <span data-ttu-id="78470-110">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="78470-110">-Detailed</span></span>
<span data-ttu-id="78470-111">이 cmdlet이 네트워크 보안 그룹에 대 한 네트워크 보안 규칙을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="78470-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

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

### <span data-ttu-id="78470-112">-이름</span><span class="sxs-lookup"><span data-stu-id="78470-112">-Name</span></span>
<span data-ttu-id="78470-113">이 cmdlet이 가져오는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78470-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="78470-114">Azure 포털을 사용 하 여 ***기본 네트워킹*** 이외의 리소스 그룹에 클래식 네트워크 보안 그룹이 만들어지면 다음 PowerShell 구문을 사용 해야 합니다 `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` .</span><span class="sxs-lookup"><span data-stu-id="78470-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

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

### <span data-ttu-id="78470-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="78470-115">-Profile</span></span>
<span data-ttu-id="78470-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78470-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78470-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="78470-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78470-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78470-118">CommonParameters</span></span>
<span data-ttu-id="78470-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78470-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78470-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78470-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78470-121">입력</span><span class="sxs-lookup"><span data-stu-id="78470-121">INPUTS</span></span>

## <span data-ttu-id="78470-122">출력</span><span class="sxs-lookup"><span data-stu-id="78470-122">OUTPUTS</span></span>

## <span data-ttu-id="78470-123">상속자</span><span class="sxs-lookup"><span data-stu-id="78470-123">NOTES</span></span>

## <span data-ttu-id="78470-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78470-124">RELATED LINKS</span></span>

[<span data-ttu-id="78470-125">새로운 AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78470-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="78470-126">제거-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="78470-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

