---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 7c385f230456da60df76c56fc652dda53362c778
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882762"
---
# <span data-ttu-id="86010-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="86010-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="86010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86010-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86010-103">구문과</span><span class="sxs-lookup"><span data-stu-id="86010-103">SYNTAX</span></span>

### <span data-ttu-id="86010-104">S1</span><span class="sxs-lookup"><span data-stu-id="86010-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86010-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="86010-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86010-106">설명은</span><span class="sxs-lookup"><span data-stu-id="86010-106">DESCRIPTION</span></span>
<span data-ttu-id="86010-107">**AzureRmWebAppSlotPublishingProfile** cmdlet은 지정 된 웹 앱 슬롯에 대 한 게시 프로필을 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="86010-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="86010-108">예제의</span><span class="sxs-lookup"><span data-stu-id="86010-108">EXAMPLES</span></span>

### <span data-ttu-id="86010-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="86010-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="86010-110">이 명령은 리소스 그룹 Default-웹용 WestUS와 연결 된 웹 앱 ContosoWebApp의 slot001 이라는 슬롯에 대 한 게시 프로필을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="86010-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="86010-111">변수</span><span class="sxs-lookup"><span data-stu-id="86010-111">PARAMETERS</span></span>

### <span data-ttu-id="86010-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86010-112">-DefaultProfile</span></span>
<span data-ttu-id="86010-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86010-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86010-114">-이름</span><span class="sxs-lookup"><span data-stu-id="86010-114">-Name</span></span>
<span data-ttu-id="86010-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="86010-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86010-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86010-116">-ResourceGroupName</span></span>
<span data-ttu-id="86010-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="86010-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86010-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="86010-118">-Slot</span></span>
<span data-ttu-id="86010-119">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="86010-119">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86010-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="86010-120">-WebApp</span></span>
<span data-ttu-id="86010-121">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="86010-121">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86010-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86010-122">CommonParameters</span></span>
<span data-ttu-id="86010-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="86010-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86010-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86010-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86010-125">입력</span><span class="sxs-lookup"><span data-stu-id="86010-125">INPUTS</span></span>

### <span data-ttu-id="86010-126">Site</span><span class="sxs-lookup"><span data-stu-id="86010-126">Site</span></span>
<span data-ttu-id="86010-127">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="86010-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="86010-128">출력</span><span class="sxs-lookup"><span data-stu-id="86010-128">OUTPUTS</span></span>

## <span data-ttu-id="86010-129">상속자</span><span class="sxs-lookup"><span data-stu-id="86010-129">NOTES</span></span>

## <span data-ttu-id="86010-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86010-130">RELATED LINKS</span></span>

