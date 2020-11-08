---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045988"
---
# <span data-ttu-id="630ec-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="630ec-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="630ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="630ec-102">SYNOPSIS</span></span>
<span data-ttu-id="630ec-103">네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-103">Creates a namespace.</span></span>

## <span data-ttu-id="630ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="630ec-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="630ec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="630ec-105">DESCRIPTION</span></span>
<span data-ttu-id="630ec-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="630ec-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="630ec-108">**AzureSBNamespace** Cmdlet은 Azure의 service Bus와 함께 사용할 서비스 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="630ec-109">예제의</span><span class="sxs-lookup"><span data-stu-id="630ec-109">EXAMPLES</span></span>

### <span data-ttu-id="630ec-110">예제 1: 서비스 네임 스페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="630ec-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="630ec-111">이 예제에서는 Azure의 Service Bus와 함께 사용할 서비스 네임 스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="630ec-112">두 예제 모두에는 필수 매개 변수 값이 포함 되지만 첫 번째 매개 변수 이름만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="630ec-113">두 매개 변수가 모두 위치이 고 해당 값이 필요한 순서 대로 제공 되기 때문에 두번째 예제를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="630ec-114">변수</span><span class="sxs-lookup"><span data-stu-id="630ec-114">PARAMETERS</span></span>

### <span data-ttu-id="630ec-115">-CreateACSNamespace 스페이스</span><span class="sxs-lookup"><span data-stu-id="630ec-115">-CreateACSNamespace</span></span>
<span data-ttu-id="630ec-116">서비스 네임 스페이스 외에도 연결 된 ACS 네임 스페이스를 만들지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="630ec-117">-위치</span><span class="sxs-lookup"><span data-stu-id="630ec-117">-Location</span></span>
<span data-ttu-id="630ec-118">새 네임 스페이스의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-118">Specifies a region for the new namespace.</span></span>

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

### <span data-ttu-id="630ec-119">-이름</span><span class="sxs-lookup"><span data-stu-id="630ec-119">-Name</span></span>
<span data-ttu-id="630ec-120">새 네임 스페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-120">Specifies a name for the new namespace.</span></span>

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

### <span data-ttu-id="630ec-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="630ec-121">-NamespaceType</span></span>
<span data-ttu-id="630ec-122">메시지 또는 알림 허브에 네임 스페이스를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="630ec-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="630ec-123">-Profile</span></span>
<span data-ttu-id="630ec-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="630ec-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="630ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630ec-126">CommonParameters</span></span>
<span data-ttu-id="630ec-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="630ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630ec-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="630ec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630ec-129">입력</span><span class="sxs-lookup"><span data-stu-id="630ec-129">INPUTS</span></span>

## <span data-ttu-id="630ec-130">출력</span><span class="sxs-lookup"><span data-stu-id="630ec-130">OUTPUTS</span></span>

## <span data-ttu-id="630ec-131">상속자</span><span class="sxs-lookup"><span data-stu-id="630ec-131">NOTES</span></span>

## <span data-ttu-id="630ec-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="630ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="630ec-133">제거-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="630ec-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)


