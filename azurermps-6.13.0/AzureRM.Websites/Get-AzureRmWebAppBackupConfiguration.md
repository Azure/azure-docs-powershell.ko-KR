---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 81c9d87ecd93097c7e114a312b68d25d7dd681c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702086"
---
# <span data-ttu-id="f7f1f-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7f1f-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f7f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f1f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7f1f-103">구문과</span><span class="sxs-lookup"><span data-stu-id="f7f1f-103">SYNTAX</span></span>

### <span data-ttu-id="f7f1f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f7f1f-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7f1f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f7f1f-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7f1f-106">설명은</span><span class="sxs-lookup"><span data-stu-id="f7f1f-106">DESCRIPTION</span></span>
<span data-ttu-id="f7f1f-107">**AzureRmWebAppBackupConfiguration** Cmdlet은 Azure Web App의 백업 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7f1f-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="f7f1f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f7f1f-108">EXAMPLES</span></span>

### <span data-ttu-id="f7f1f-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="f7f1f-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="f7f1f-110">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 이라는 웹 앱에서 백업 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7f1f-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f7f1f-111">변수</span><span class="sxs-lookup"><span data-stu-id="f7f1f-111">PARAMETERS</span></span>

### <span data-ttu-id="f7f1f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f1f-112">-DefaultProfile</span></span>
<span data-ttu-id="f7f1f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7f1f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7f1f-114">-이름</span><span class="sxs-lookup"><span data-stu-id="f7f1f-114">-Name</span></span>
<span data-ttu-id="f7f1f-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="f7f1f-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f1f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f1f-116">-ResourceGroupName</span></span>
<span data-ttu-id="f7f1f-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f7f1f-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f1f-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="f7f1f-118">-Slot</span></span>
<span data-ttu-id="f7f1f-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="f7f1f-119">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f1f-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="f7f1f-120">-WebApp</span></span>
<span data-ttu-id="f7f1f-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="f7f1f-121">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f1f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f1f-122">CommonParameters</span></span>
<span data-ttu-id="f7f1f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7f1f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f1f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f1f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f1f-125">입력</span><span class="sxs-lookup"><span data-stu-id="f7f1f-125">INPUTS</span></span>

### <span data-ttu-id="f7f1f-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f7f1f-126">System.String</span></span>

### <span data-ttu-id="f7f1f-127">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="f7f1f-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="f7f1f-128">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f7f1f-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="f7f1f-129">출력</span><span class="sxs-lookup"><span data-stu-id="f7f1f-129">OUTPUTS</span></span>

### <span data-ttu-id="f7f1f-130">AzureWebAppBackupConfiguration (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="f7f1f-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f7f1f-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f7f1f-131">NOTES</span></span>

## <span data-ttu-id="f7f1f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7f1f-132">RELATED LINKS</span></span>
