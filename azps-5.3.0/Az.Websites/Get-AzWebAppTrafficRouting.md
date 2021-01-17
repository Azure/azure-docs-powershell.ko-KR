---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491465"
---
# <span data-ttu-id="30452-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="30452-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="30452-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30452-102">SYNOPSIS</span></span>
<span data-ttu-id="30452-103">주어진 슬롯 이름에 대한 라우팅 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30452-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="30452-104">구문</span><span class="sxs-lookup"><span data-stu-id="30452-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30452-105">설명</span><span class="sxs-lookup"><span data-stu-id="30452-105">DESCRIPTION</span></span>
<span data-ttu-id="30452-106">**Get-AzWebAppTrafficRouting** cmdlet은 Azure 웹앱 슬롯에서 라우팅 규칙 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30452-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="30452-107">예제</span><span class="sxs-lookup"><span data-stu-id="30452-107">EXAMPLES</span></span>

### <span data-ttu-id="30452-108">예제 1 웹앱 슬롯에서 특정 라우팅 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30452-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="30452-109">이 명령은 주어진 웹앱 슬롯에 대한 라우팅 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="30452-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="30452-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30452-110">PARAMETERS</span></span>

### <span data-ttu-id="30452-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30452-111">-DefaultProfile</span></span>
<span data-ttu-id="30452-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30452-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30452-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30452-113">-ResourceGroupName</span></span>
<span data-ttu-id="30452-114">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="30452-114">Resource Group Name</span></span>

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

### <span data-ttu-id="30452-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="30452-115">-RuleName</span></span>
<span data-ttu-id="30452-116">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="30452-116">Rule Name</span></span>
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

### <span data-ttu-id="30452-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="30452-117">-WebAppName</span></span>
<span data-ttu-id="30452-118">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="30452-118">WebApp Name</span></span>

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

### <span data-ttu-id="30452-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30452-119">CommonParameters</span></span>
<span data-ttu-id="30452-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30452-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30452-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30452-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30452-122">입력</span><span class="sxs-lookup"><span data-stu-id="30452-122">INPUTS</span></span>

### <span data-ttu-id="30452-123">없음</span><span class="sxs-lookup"><span data-stu-id="30452-123">None</span></span>

## <span data-ttu-id="30452-124">출력</span><span class="sxs-lookup"><span data-stu-id="30452-124">OUTPUTS</span></span>

### <span data-ttu-id="30452-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="30452-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="30452-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30452-126">NOTES</span></span>

## <span data-ttu-id="30452-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30452-127">RELATED LINKS</span></span>

[<span data-ttu-id="30452-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="30452-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="30452-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="30452-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="30452-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="30452-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
