---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045613"
---
# <span data-ttu-id="4bd5c-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="4bd5c-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="4bd5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd5c-103">네임 스페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bd5c-103">Gets the namespace.</span></span>


## <span data-ttu-id="4bd5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4bd5c-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4bd5c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4bd5c-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd5c-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bd5c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="4bd5c-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bd5c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="4bd5c-108">**Get-AzureSBNamespace** cmdlet은 현재 구독과 연결 된 service Bus 서비스 네임 스페이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bd5c-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="4bd5c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4bd5c-109">EXAMPLES</span></span>

### <span data-ttu-id="4bd5c-110">예제 1: Service Bus 네임 스페이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="4bd5c-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="4bd5c-111">이 예제에서는 현재 구독과 연결 된 Service Bus 서비스 네임 스페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4bd5c-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="4bd5c-112">변수</span><span class="sxs-lookup"><span data-stu-id="4bd5c-112">PARAMETERS</span></span>

### <span data-ttu-id="4bd5c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="4bd5c-113">-Name</span></span>
<span data-ttu-id="4bd5c-114">찾을 서비스 버스 네임 스페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bd5c-114">Specifies the name of a Service Bus namespace to look for.</span></span>

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

### <span data-ttu-id="4bd5c-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="4bd5c-115">-Profile</span></span>
<span data-ttu-id="4bd5c-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bd5c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4bd5c-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4bd5c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4bd5c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd5c-118">CommonParameters</span></span>
<span data-ttu-id="4bd5c-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4bd5c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd5c-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd5c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd5c-121">입력</span><span class="sxs-lookup"><span data-stu-id="4bd5c-121">INPUTS</span></span>

## <span data-ttu-id="4bd5c-122">출력</span><span class="sxs-lookup"><span data-stu-id="4bd5c-122">OUTPUTS</span></span>

## <span data-ttu-id="4bd5c-123">상속자</span><span class="sxs-lookup"><span data-stu-id="4bd5c-123">NOTES</span></span>

## <span data-ttu-id="4bd5c-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bd5c-124">RELATED LINKS</span></span>

[<span data-ttu-id="4bd5c-125">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="4bd5c-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)


