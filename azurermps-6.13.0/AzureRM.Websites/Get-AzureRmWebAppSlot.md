---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: f7be5b7877362484d0f3dfe4d19b8afc669e917c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524212"
---
# <span data-ttu-id="13ca2-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13ca2-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="13ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="13ca2-103">Azure 웹 앱 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13ca2-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13ca2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13ca2-104">SYNTAX</span></span>

### <span data-ttu-id="13ca2-105">S1</span><span class="sxs-lookup"><span data-stu-id="13ca2-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ca2-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="13ca2-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13ca2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="13ca2-107">DESCRIPTION</span></span>
<span data-ttu-id="13ca2-108">**AzureRmWebAppSlot** Cmdlet은 Azure Web App 슬롯에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13ca2-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="13ca2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="13ca2-109">EXAMPLES</span></span>

### <span data-ttu-id="13ca2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="13ca2-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="13ca2-111">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 라는 웹 앱에서 Slot001 라는 슬롯을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13ca2-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="13ca2-112">변수</span><span class="sxs-lookup"><span data-stu-id="13ca2-112">PARAMETERS</span></span>

### <span data-ttu-id="13ca2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ca2-113">-DefaultProfile</span></span>
<span data-ttu-id="13ca2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13ca2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ca2-115">-이름</span><span class="sxs-lookup"><span data-stu-id="13ca2-115">-Name</span></span>
<span data-ttu-id="13ca2-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="13ca2-116">WebApp Name</span></span>

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

### <span data-ttu-id="13ca2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ca2-117">-ResourceGroupName</span></span>
<span data-ttu-id="13ca2-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="13ca2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="13ca2-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="13ca2-119">-Slot</span></span>
<span data-ttu-id="13ca2-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="13ca2-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="13ca2-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="13ca2-121">-WebApp</span></span>
<span data-ttu-id="13ca2-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="13ca2-122">WebApp Object</span></span>

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

### <span data-ttu-id="13ca2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ca2-123">CommonParameters</span></span>
<span data-ttu-id="13ca2-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13ca2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ca2-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ca2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ca2-126">입력</span><span class="sxs-lookup"><span data-stu-id="13ca2-126">INPUTS</span></span>

### <span data-ttu-id="13ca2-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13ca2-127">System.String</span></span>

### <span data-ttu-id="13ca2-128">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="13ca2-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="13ca2-129">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13ca2-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="13ca2-130">출력</span><span class="sxs-lookup"><span data-stu-id="13ca2-130">OUTPUTS</span></span>

### <span data-ttu-id="13ca2-131">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="13ca2-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="13ca2-132">상속자</span><span class="sxs-lookup"><span data-stu-id="13ca2-132">NOTES</span></span>

## <span data-ttu-id="13ca2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13ca2-133">RELATED LINKS</span></span>

[<span data-ttu-id="13ca2-134">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13ca2-134">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="13ca2-135">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13ca2-135">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="13ca2-136">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13ca2-136">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="13ca2-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13ca2-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="13ca2-138">시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13ca2-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="13ca2-139">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="13ca2-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="13ca2-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="13ca2-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
