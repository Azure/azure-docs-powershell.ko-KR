---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7ABEC06E-1046-401E-B4A1-902FC3EED867
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0f0ff81fc38916adeedbb495117a8b27a1f88fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045948"
---
# <span data-ttu-id="30580-101">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="30580-101">Show-AzurePortal</span></span>

## <span data-ttu-id="30580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30580-102">SYNOPSIS</span></span>
<span data-ttu-id="30580-103">Azure 관리 포털을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30580-103">Show the Azure Management Portal.</span></span>

## <span data-ttu-id="30580-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30580-104">SYNTAX</span></span>

```
Show-AzurePortal [-Name <String>] [-Realm <String>] [-Environment <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="30580-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30580-105">DESCRIPTION</span></span>
<span data-ttu-id="30580-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="30580-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="30580-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="30580-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="30580-108">**AzurePortal** Cmdlet은 Azure 관리 포털을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30580-108">The **Show-AzurePortal** cmdlet shows the Azure Management Portal.</span></span>

## <span data-ttu-id="30580-109">예제의</span><span class="sxs-lookup"><span data-stu-id="30580-109">EXAMPLES</span></span>

### <span data-ttu-id="30580-110">예제 1: 웹 사이트에 대 한 정보 표시</span><span class="sxs-lookup"><span data-stu-id="30580-110">Example 1: Show information about a web site</span></span>
```
PS C:\> Show-AzurePortal -Name mySite
```

<span data-ttu-id="30580-111">이 예제에서는 Azure 포털에서 브라우저가 열려 있는 웹 사이트에 대 한 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30580-111">This example opens a browser on the Azure portal, showing information about a web site named mySite.</span></span>

## <span data-ttu-id="30580-112">변수</span><span class="sxs-lookup"><span data-stu-id="30580-112">PARAMETERS</span></span>

### <span data-ttu-id="30580-113">-환경</span><span class="sxs-lookup"><span data-stu-id="30580-113">-Environment</span></span>
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

### <span data-ttu-id="30580-114">-이름</span><span class="sxs-lookup"><span data-stu-id="30580-114">-Name</span></span>
<span data-ttu-id="30580-115">포털에 표시할 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30580-115">Specifies the name of the website to show in the portal.</span></span>

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

### <span data-ttu-id="30580-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="30580-116">-Profile</span></span>
<span data-ttu-id="30580-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30580-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30580-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="30580-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30580-119">-영역</span><span class="sxs-lookup"><span data-stu-id="30580-119">-Realm</span></span>
<span data-ttu-id="30580-120">Azure 포털을 표시할 때 페더레이션 인증에 사용할 조직 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30580-120">Specifies the organization ID to use for federated authentication when displaying the Azure Portal.</span></span>

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

### <span data-ttu-id="30580-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30580-121">CommonParameters</span></span>
<span data-ttu-id="30580-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30580-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30580-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30580-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30580-124">입력</span><span class="sxs-lookup"><span data-stu-id="30580-124">INPUTS</span></span>

## <span data-ttu-id="30580-125">출력</span><span class="sxs-lookup"><span data-stu-id="30580-125">OUTPUTS</span></span>

## <span data-ttu-id="30580-126">상속자</span><span class="sxs-lookup"><span data-stu-id="30580-126">NOTES</span></span>

## <span data-ttu-id="30580-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30580-127">RELATED LINKS</span></span>

[<span data-ttu-id="30580-128">쇼-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="30580-128">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


