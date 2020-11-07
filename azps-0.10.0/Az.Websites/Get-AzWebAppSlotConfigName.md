---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 414e25840b03127bbe94586248641e103c1f7d88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876144"
---
# <span data-ttu-id="8919a-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="8919a-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="8919a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8919a-102">SYNOPSIS</span></span>
<span data-ttu-id="8919a-103">웹 앱 슬롯 구성 이름 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="8919a-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="8919a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8919a-104">SYNTAX</span></span>

### <span data-ttu-id="8919a-105">S1</span><span class="sxs-lookup"><span data-stu-id="8919a-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8919a-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="8919a-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8919a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8919a-107">DESCRIPTION</span></span>
<span data-ttu-id="8919a-108">**AzWebAppSlotConfigName** cmdlet은 현재 슬롯 설정으로 표시 된 앱 설정 및 연결 문자열 이름 목록을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8919a-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="8919a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8919a-109">EXAMPLES</span></span>

### <span data-ttu-id="8919a-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="8919a-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8919a-111">이 명령은 리소스 그룹 기본값과 연결 된 ContosoSite 이라는 웹 앱에 관련 된 앱 설정 및 연결 문자열을 가져옵니다. WestUS</span><span class="sxs-lookup"><span data-stu-id="8919a-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="8919a-112">변수</span><span class="sxs-lookup"><span data-stu-id="8919a-112">PARAMETERS</span></span>

### <span data-ttu-id="8919a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8919a-113">-DefaultProfile</span></span>
<span data-ttu-id="8919a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8919a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8919a-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8919a-115">-Name</span></span>
<span data-ttu-id="8919a-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="8919a-116">WebApp Name</span></span>

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

### <span data-ttu-id="8919a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8919a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8919a-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8919a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8919a-119">-Web app</span><span class="sxs-lookup"><span data-stu-id="8919a-119">-WebApp</span></span>
<span data-ttu-id="8919a-120">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="8919a-120">WebApp Object</span></span>

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

### <span data-ttu-id="8919a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8919a-121">CommonParameters</span></span>
<span data-ttu-id="8919a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8919a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8919a-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8919a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8919a-124">입력</span><span class="sxs-lookup"><span data-stu-id="8919a-124">INPUTS</span></span>

### <span data-ttu-id="8919a-125">Site</span><span class="sxs-lookup"><span data-stu-id="8919a-125">Site</span></span>
<span data-ttu-id="8919a-126">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8919a-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8919a-127">출력</span><span class="sxs-lookup"><span data-stu-id="8919a-127">OUTPUTS</span></span>

## <span data-ttu-id="8919a-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8919a-128">NOTES</span></span>

## <span data-ttu-id="8919a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8919a-129">RELATED LINKS</span></span>

