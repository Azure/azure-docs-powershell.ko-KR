---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326913"
---
# <span data-ttu-id="8761d-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8761d-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="8761d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8761d-102">SYNOPSIS</span></span>
<span data-ttu-id="8761d-103">Azure Web App에 대한 Access Restiction 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8761d-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="8761d-104">구문</span><span class="sxs-lookup"><span data-stu-id="8761d-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8761d-105">설명</span><span class="sxs-lookup"><span data-stu-id="8761d-105">DESCRIPTION</span></span>
<span data-ttu-id="8761d-106">**Get-AzWebAppAccessRestrictionConfig** cmdlet은 Azure 웹앱에 대한 액세스 제한 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8761d-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="8761d-107">예제</span><span class="sxs-lookup"><span data-stu-id="8761d-107">EXAMPLES</span></span>

### <span data-ttu-id="8761d-108">예제 1: 리소스 그룹에서 웹앱 액세스 제한 구성을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="8761d-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="8761d-109">이 명령은 리소스 그룹 Default-Web-WestUS에 속하는 ContosoSite라는 웹앱의 액세스 제한 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8761d-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8761d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8761d-110">PARAMETERS</span></span>

### <span data-ttu-id="8761d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8761d-111">-DefaultProfile</span></span>
<span data-ttu-id="8761d-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8761d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8761d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8761d-113">-Name</span></span>
<span data-ttu-id="8761d-114">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="8761d-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8761d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8761d-115">-ResourceGroupName</span></span>
<span data-ttu-id="8761d-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8761d-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8761d-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="8761d-117">-SlotName</span></span>
<span data-ttu-id="8761d-118">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8761d-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8761d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8761d-119">CommonParameters</span></span>
<span data-ttu-id="8761d-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8761d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8761d-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8761d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8761d-122">입력</span><span class="sxs-lookup"><span data-stu-id="8761d-122">INPUTS</span></span>

### <span data-ttu-id="8761d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8761d-123">System.String</span></span>

## <span data-ttu-id="8761d-124">출력</span><span class="sxs-lookup"><span data-stu-id="8761d-124">OUTPUTS</span></span>

### <span data-ttu-id="8761d-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8761d-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="8761d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8761d-126">NOTES</span></span>

## <span data-ttu-id="8761d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8761d-127">RELATED LINKS</span></span>

[<span data-ttu-id="8761d-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8761d-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="8761d-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="8761d-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="8761d-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="8761d-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
