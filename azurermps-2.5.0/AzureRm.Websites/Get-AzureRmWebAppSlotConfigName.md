---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: ff05a30c495475b63b0385f3398c78e0b018a4bc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882114"
---
# <span data-ttu-id="804f1-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="804f1-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="804f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="804f1-102">SYNOPSIS</span></span>
<span data-ttu-id="804f1-103">웹 앱 슬롯 구성 이름 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="804f1-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="804f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="804f1-104">SYNTAX</span></span>

### <span data-ttu-id="804f1-105">S1</span><span class="sxs-lookup"><span data-stu-id="804f1-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="804f1-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="804f1-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="804f1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="804f1-107">DESCRIPTION</span></span>
<span data-ttu-id="804f1-108">**AzureRmWebAppSlotConfigName** cmdlet은 현재 슬롯 설정으로 표시 된 앱 설정 및 연결 문자열 이름 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="804f1-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="804f1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="804f1-109">EXAMPLES</span></span>

### <span data-ttu-id="804f1-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="804f1-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="804f1-111">이 명령은 리소스 그룹 기본값과 연결 된 ContosoSite 이라는 웹 앱에 관련 된 앱 설정 및 연결 문자열을 가져옵니다. WestUS</span><span class="sxs-lookup"><span data-stu-id="804f1-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="804f1-112">변수</span><span class="sxs-lookup"><span data-stu-id="804f1-112">PARAMETERS</span></span>

### <span data-ttu-id="804f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804f1-113">-DefaultProfile</span></span>
<span data-ttu-id="804f1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="804f1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="804f1-115">-이름</span><span class="sxs-lookup"><span data-stu-id="804f1-115">-Name</span></span>
<span data-ttu-id="804f1-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="804f1-116">WebApp Name</span></span>

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

### <span data-ttu-id="804f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="804f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="804f1-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="804f1-118">Resource Group Name</span></span>

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

### <span data-ttu-id="804f1-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="804f1-119">-WebApp</span></span>
<span data-ttu-id="804f1-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="804f1-120">WebApp Object</span></span>

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

### <span data-ttu-id="804f1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804f1-121">CommonParameters</span></span>
<span data-ttu-id="804f1-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="804f1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804f1-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="804f1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804f1-124">입력</span><span class="sxs-lookup"><span data-stu-id="804f1-124">INPUTS</span></span>

### <span data-ttu-id="804f1-125">Site</span><span class="sxs-lookup"><span data-stu-id="804f1-125">Site</span></span>
<span data-ttu-id="804f1-126">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="804f1-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="804f1-127">출력</span><span class="sxs-lookup"><span data-stu-id="804f1-127">OUTPUTS</span></span>

## <span data-ttu-id="804f1-128">상속자</span><span class="sxs-lookup"><span data-stu-id="804f1-128">NOTES</span></span>

## <span data-ttu-id="804f1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="804f1-129">RELATED LINKS</span></span>

