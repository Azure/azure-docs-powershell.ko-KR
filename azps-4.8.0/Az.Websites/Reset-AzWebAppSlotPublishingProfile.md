---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056012"
---
# <span data-ttu-id="29e03-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="29e03-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="29e03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29e03-102">SYNOPSIS</span></span>

## <span data-ttu-id="29e03-103">구문과</span><span class="sxs-lookup"><span data-stu-id="29e03-103">SYNTAX</span></span>

### <span data-ttu-id="29e03-104">S1</span><span class="sxs-lookup"><span data-stu-id="29e03-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29e03-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="29e03-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29e03-106">설명은</span><span class="sxs-lookup"><span data-stu-id="29e03-106">DESCRIPTION</span></span>
<span data-ttu-id="29e03-107">**AzWebAppSlotPublishingProfile** cmdlet은 지정 된 웹 앱 슬롯에 대 한 게시 프로필을 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e03-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="29e03-108">예제의</span><span class="sxs-lookup"><span data-stu-id="29e03-108">EXAMPLES</span></span>

### <span data-ttu-id="29e03-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="29e03-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="29e03-110">이 명령은 리소스 그룹 Default-웹용 WestUS와 연결 된 웹 앱 ContosoWebApp의 slot001 이라는 슬롯에 대 한 게시 프로필을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e03-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="29e03-111">변수</span><span class="sxs-lookup"><span data-stu-id="29e03-111">PARAMETERS</span></span>

### <span data-ttu-id="29e03-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e03-112">-DefaultProfile</span></span>
<span data-ttu-id="29e03-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29e03-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29e03-114">-이름</span><span class="sxs-lookup"><span data-stu-id="29e03-114">-Name</span></span>
<span data-ttu-id="29e03-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="29e03-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e03-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29e03-116">-ResourceGroupName</span></span>
<span data-ttu-id="29e03-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="29e03-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e03-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="29e03-118">-Slot</span></span>
<span data-ttu-id="29e03-119">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="29e03-119">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e03-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="29e03-120">-WebApp</span></span>
<span data-ttu-id="29e03-121">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="29e03-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29e03-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e03-122">CommonParameters</span></span>
<span data-ttu-id="29e03-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="29e03-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e03-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e03-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e03-125">입력</span><span class="sxs-lookup"><span data-stu-id="29e03-125">INPUTS</span></span>

### <span data-ttu-id="29e03-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="29e03-126">System.String</span></span>

### <span data-ttu-id="29e03-127">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="29e03-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="29e03-128">출력</span><span class="sxs-lookup"><span data-stu-id="29e03-128">OUTPUTS</span></span>

### <span data-ttu-id="29e03-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="29e03-129">System.String</span></span>

## <span data-ttu-id="29e03-130">상속자</span><span class="sxs-lookup"><span data-stu-id="29e03-130">NOTES</span></span>

## <span data-ttu-id="29e03-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29e03-131">RELATED LINKS</span></span>
