---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: 089711bacd6401b4c44683a159e43a92a56106d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525875"
---
# <span data-ttu-id="53549-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53549-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="53549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53549-102">SYNOPSIS</span></span>
<span data-ttu-id="53549-103">Azure Web App 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="53549-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53549-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53549-104">SYNTAX</span></span>

### <span data-ttu-id="53549-105">S1</span><span class="sxs-lookup"><span data-stu-id="53549-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53549-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="53549-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53549-107">설명은</span><span class="sxs-lookup"><span data-stu-id="53549-107">DESCRIPTION</span></span>
<span data-ttu-id="53549-108">**AzureRmWebAppSlot** Cmdlet은 Azure Web App 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="53549-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="53549-109">예제의</span><span class="sxs-lookup"><span data-stu-id="53549-109">EXAMPLES</span></span>

### <span data-ttu-id="53549-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="53549-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="53549-111">이 명령은 Default-WestUS 이라는 리소스 그룹에 속하는 ContosoWebApp 이라는 웹 앱에 대 한 Slot001 이라는 슬롯을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="53549-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="53549-112">변수</span><span class="sxs-lookup"><span data-stu-id="53549-112">PARAMETERS</span></span>

### <span data-ttu-id="53549-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53549-113">-DefaultProfile</span></span>
<span data-ttu-id="53549-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53549-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53549-115">-이름</span><span class="sxs-lookup"><span data-stu-id="53549-115">-Name</span></span>
<span data-ttu-id="53549-116">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="53549-116">WebApp Name</span></span>

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

### <span data-ttu-id="53549-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53549-117">-ResourceGroupName</span></span>
<span data-ttu-id="53549-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="53549-118">Resource Group Name</span></span>

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

### <span data-ttu-id="53549-119">-슬롯</span><span class="sxs-lookup"><span data-stu-id="53549-119">-Slot</span></span>
<span data-ttu-id="53549-120">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="53549-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53549-121">-Web app</span><span class="sxs-lookup"><span data-stu-id="53549-121">-WebApp</span></span>
<span data-ttu-id="53549-122">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="53549-122">WebApp Object</span></span>

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

### <span data-ttu-id="53549-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53549-123">CommonParameters</span></span>
<span data-ttu-id="53549-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53549-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53549-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53549-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53549-126">입력</span><span class="sxs-lookup"><span data-stu-id="53549-126">INPUTS</span></span>

### <span data-ttu-id="53549-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="53549-127">System.String</span></span>

### <span data-ttu-id="53549-128">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="53549-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="53549-129">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53549-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="53549-130">출력</span><span class="sxs-lookup"><span data-stu-id="53549-130">OUTPUTS</span></span>

### <span data-ttu-id="53549-131">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="53549-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="53549-132">상속자</span><span class="sxs-lookup"><span data-stu-id="53549-132">NOTES</span></span>

## <span data-ttu-id="53549-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53549-133">RELATED LINKS</span></span>

[<span data-ttu-id="53549-134">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53549-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="53549-135">새로운 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53549-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="53549-136">제거-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53549-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="53549-137">다시 시작-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53549-137">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="53549-138">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53549-138">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="53549-139">중지-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53549-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="53549-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="53549-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
