---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217120"
---
# <span data-ttu-id="b3c6a-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b3c6a-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="b3c6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c6a-103">지정 된 슬롯 이름에 대 한 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3c6a-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="b3c6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3c6a-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3c6a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b3c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c6a-106">**AzWebAppTrafficRouting** Cmdlet은 Azure Web App 슬롯에서 라우팅 규칙 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3c6a-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="b3c6a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b3c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="b3c6a-108">예제 1 web app 슬롯에서 특정 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3c6a-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="b3c6a-109">이 명령은 지정 된 web app 슬롯에 대 한 라우팅 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3c6a-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="b3c6a-110">변수</span><span class="sxs-lookup"><span data-stu-id="b3c6a-110">PARAMETERS</span></span>

### <span data-ttu-id="b3c6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c6a-111">-DefaultProfile</span></span>
<span data-ttu-id="b3c6a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3c6a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3c6a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c6a-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3c6a-114">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b3c6a-114">Resource Group Name</span></span>

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

### <span data-ttu-id="b3c6a-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="b3c6a-115">-RuleName</span></span>
<span data-ttu-id="b3c6a-116">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="b3c6a-116">Rule Name</span></span>
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

### <span data-ttu-id="b3c6a-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="b3c6a-117">-WebAppName</span></span>
<span data-ttu-id="b3c6a-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="b3c6a-118">WebApp Name</span></span>

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

### <span data-ttu-id="b3c6a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c6a-119">CommonParameters</span></span>
<span data-ttu-id="b3c6a-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3c6a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c6a-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3c6a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c6a-122">입력</span><span class="sxs-lookup"><span data-stu-id="b3c6a-122">INPUTS</span></span>

### <span data-ttu-id="b3c6a-123">않아야</span><span class="sxs-lookup"><span data-stu-id="b3c6a-123">None</span></span>

## <span data-ttu-id="b3c6a-124">출력</span><span class="sxs-lookup"><span data-stu-id="b3c6a-124">OUTPUTS</span></span>

### <span data-ttu-id="b3c6a-125">RampUpRule/. m i.</span><span class="sxs-lookup"><span data-stu-id="b3c6a-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="b3c6a-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b3c6a-126">NOTES</span></span>

## <span data-ttu-id="b3c6a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3c6a-127">RELATED LINKS</span></span>

[<span data-ttu-id="b3c6a-128">업데이트-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b3c6a-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b3c6a-129">추가-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b3c6a-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="b3c6a-130">제거-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="b3c6a-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
