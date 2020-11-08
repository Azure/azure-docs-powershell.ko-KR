---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213432"
---
# <span data-ttu-id="578ca-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="578ca-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="578ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="578ca-102">SYNOPSIS</span></span>
<span data-ttu-id="578ca-103">지정 된 슬롯 이름에 대 한 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="578ca-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="578ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="578ca-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="578ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="578ca-105">DESCRIPTION</span></span>
<span data-ttu-id="578ca-106">**AzWebAppTrafficRouting** Cmdlet은 Azure Web App 슬롯에서 라우팅 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="578ca-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="578ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="578ca-107">EXAMPLES</span></span>

### <span data-ttu-id="578ca-108">예제 1 web app 슬롯에서 특정 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="578ca-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="578ca-109">이 명령은 지정 된 web app 슬롯에 대 한 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="578ca-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="578ca-110">변수</span><span class="sxs-lookup"><span data-stu-id="578ca-110">PARAMETERS</span></span>

### <span data-ttu-id="578ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578ca-111">-DefaultProfile</span></span>
<span data-ttu-id="578ca-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="578ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="578ca-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578ca-113">-ResourceGroupName</span></span>
<span data-ttu-id="578ca-114">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="578ca-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="578ca-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="578ca-115">-RuleName</span></span>
<span data-ttu-id="578ca-116">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="578ca-116">Rule Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="578ca-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="578ca-117">-WebAppName</span></span>
<span data-ttu-id="578ca-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="578ca-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="578ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578ca-119">CommonParameters</span></span>
<span data-ttu-id="578ca-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="578ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578ca-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="578ca-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578ca-122">입력</span><span class="sxs-lookup"><span data-stu-id="578ca-122">INPUTS</span></span>

### <span data-ttu-id="578ca-123">않아야</span><span class="sxs-lookup"><span data-stu-id="578ca-123">None</span></span>

## <span data-ttu-id="578ca-124">출력</span><span class="sxs-lookup"><span data-stu-id="578ca-124">OUTPUTS</span></span>

### <span data-ttu-id="578ca-125">RampUpRule/. m i.</span><span class="sxs-lookup"><span data-stu-id="578ca-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="578ca-126">상속자</span><span class="sxs-lookup"><span data-stu-id="578ca-126">NOTES</span></span>

## <span data-ttu-id="578ca-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="578ca-127">RELATED LINKS</span></span>

[<span data-ttu-id="578ca-128">업데이트-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="578ca-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="578ca-129">추가-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="578ca-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="578ca-130">제거-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="578ca-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
