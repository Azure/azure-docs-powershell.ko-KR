---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877990"
---
# <span data-ttu-id="2dc52-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="2dc52-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="2dc52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dc52-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc52-103">Azure Web App에 대 한 액세스 Restiction 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2dc52-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="2dc52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2dc52-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dc52-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2dc52-105">DESCRIPTION</span></span>
<span data-ttu-id="2dc52-106">**AzWebAppAccessRestrictionConfig** Cmdlet은 Azure 웹 앱에 대 한 액세스 제한 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2dc52-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="2dc52-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2dc52-107">EXAMPLES</span></span>

### <span data-ttu-id="2dc52-108">예제 1: 리소스 그룹에서 웹 앱 액세스 제한 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="2dc52-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="2dc52-109">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 ContosoSite 이라는 웹 앱의 액세스 제한 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2dc52-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="2dc52-110">변수</span><span class="sxs-lookup"><span data-stu-id="2dc52-110">PARAMETERS</span></span>

### <span data-ttu-id="2dc52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc52-111">-DefaultProfile</span></span>
<span data-ttu-id="2dc52-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2dc52-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dc52-113">-이름</span><span class="sxs-lookup"><span data-stu-id="2dc52-113">-Name</span></span>
<span data-ttu-id="2dc52-114">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="2dc52-114">WebApp Name</span></span>

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

### <span data-ttu-id="2dc52-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc52-115">-ResourceGroupName</span></span>
<span data-ttu-id="2dc52-116">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2dc52-116">Resource Group Name</span></span>

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

### <span data-ttu-id="2dc52-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="2dc52-117">-SlotName</span></span>
<span data-ttu-id="2dc52-118">배포 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2dc52-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="2dc52-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc52-119">CommonParameters</span></span>
<span data-ttu-id="2dc52-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dc52-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc52-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2dc52-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc52-122">입력</span><span class="sxs-lookup"><span data-stu-id="2dc52-122">INPUTS</span></span>

### <span data-ttu-id="2dc52-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2dc52-123">System.String</span></span>

## <span data-ttu-id="2dc52-124">출력</span><span class="sxs-lookup"><span data-stu-id="2dc52-124">OUTPUTS</span></span>

### <span data-ttu-id="2dc52-125">PSAccessRestrictionConfig를 다운로드 하세요.</span><span class="sxs-lookup"><span data-stu-id="2dc52-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="2dc52-126">상속자</span><span class="sxs-lookup"><span data-stu-id="2dc52-126">NOTES</span></span>

## <span data-ttu-id="2dc52-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dc52-127">RELATED LINKS</span></span>

[<span data-ttu-id="2dc52-128">업데이트-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="2dc52-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="2dc52-129">추가-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="2dc52-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="2dc52-130">제거-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="2dc52-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
