---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331989"
---
# <span data-ttu-id="f2120-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="f2120-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="f2120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2120-102">SYNOPSIS</span></span>
<span data-ttu-id="f2120-103">웹앱 슬롯 구성 이름 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2120-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="f2120-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2120-104">SYNTAX</span></span>

### <span data-ttu-id="f2120-105">S1</span><span class="sxs-lookup"><span data-stu-id="f2120-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2120-106">S2</span><span class="sxs-lookup"><span data-stu-id="f2120-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2120-107">설명</span><span class="sxs-lookup"><span data-stu-id="f2120-107">DESCRIPTION</span></span>
<span data-ttu-id="f2120-108">**Get-AzWebAppSlotConfigName** cmdlet은 현재 슬롯 설정으로 표시된 앱 설정 및 연결 문자열 이름 목록을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f2120-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="f2120-109">예제</span><span class="sxs-lookup"><span data-stu-id="f2120-109">EXAMPLES</span></span>

### <span data-ttu-id="f2120-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2120-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f2120-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 ContosoSite라는 웹앱과 관련된 앱 설정 및 연결 문자열을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f2120-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="f2120-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2120-112">PARAMETERS</span></span>

### <span data-ttu-id="f2120-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2120-113">-DefaultProfile</span></span>
<span data-ttu-id="f2120-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2120-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2120-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f2120-115">-Name</span></span>
<span data-ttu-id="f2120-116">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="f2120-116">WebApp Name</span></span>

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

### <span data-ttu-id="f2120-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2120-117">-ResourceGroupName</span></span>
<span data-ttu-id="f2120-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f2120-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f2120-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f2120-119">-WebApp</span></span>
<span data-ttu-id="f2120-120">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="f2120-120">WebApp Object</span></span>

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

### <span data-ttu-id="f2120-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2120-121">CommonParameters</span></span>
<span data-ttu-id="f2120-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2120-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2120-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f2120-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2120-124">입력</span><span class="sxs-lookup"><span data-stu-id="f2120-124">INPUTS</span></span>

### <span data-ttu-id="f2120-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f2120-125">System.String</span></span>

### <span data-ttu-id="f2120-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f2120-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f2120-127">출력</span><span class="sxs-lookup"><span data-stu-id="f2120-127">OUTPUTS</span></span>

### <span data-ttu-id="f2120-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="f2120-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="f2120-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2120-129">NOTES</span></span>

## <span data-ttu-id="f2120-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2120-130">RELATED LINKS</span></span>
