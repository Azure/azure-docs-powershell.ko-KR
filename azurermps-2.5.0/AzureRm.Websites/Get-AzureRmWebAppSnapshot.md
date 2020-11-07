---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880605"
---
# <span data-ttu-id="f3f96-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f3f96-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="f3f96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f96-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f96-103">웹 앱에 사용할 수 있는 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3f96-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3f96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3f96-104">SYNTAX</span></span>

### <span data-ttu-id="f3f96-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f3f96-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="f3f96-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f3f96-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="f3f96-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f3f96-107">DESCRIPTION</span></span>
<span data-ttu-id="f3f96-108">**AzureRmWebAppSnapshot** cmdlet은 웹 앱에 대 한 모든 스냅숏을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3f96-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="f3f96-109">스냅숏은 웹 앱의 파일 및 설정에 대 한 자동 백업입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f96-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="f3f96-110">스냅숏은 **Restore-AzureRmWebAppSnapshot** cmdlet을 사용 하 여 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3f96-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="f3f96-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f3f96-111">EXAMPLES</span></span>

### <span data-ttu-id="f3f96-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3f96-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="f3f96-113">"기본-웹-WestUS" 리소스 그룹에서 "준비" 라는 슬롯을 사용 하 여 "ConstosoApp" 라는 웹 앱에 대 한 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3f96-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="f3f96-114">변수</span><span class="sxs-lookup"><span data-stu-id="f3f96-114">PARAMETERS</span></span>

### <span data-ttu-id="f3f96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f96-115">-DefaultProfile</span></span>
<span data-ttu-id="f3f96-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f96-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f3f96-117">-Name</span></span>
<span data-ttu-id="f3f96-118">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f96-118">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f96-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3f96-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f96-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f96-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="f3f96-121">-Slot</span></span>
<span data-ttu-id="f3f96-122">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3f96-122">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f96-123">-Web app</span><span class="sxs-lookup"><span data-stu-id="f3f96-123">-WebApp</span></span>
<span data-ttu-id="f3f96-124">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="f3f96-124">The web app object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## <span data-ttu-id="f3f96-125">입력</span><span class="sxs-lookup"><span data-stu-id="f3f96-125">INPUTS</span></span>

### <span data-ttu-id="f3f96-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3f96-126">System.String</span></span>
<span data-ttu-id="f3f96-127">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="f3f96-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="f3f96-128">출력</span><span class="sxs-lookup"><span data-stu-id="f3f96-128">OUTPUTS</span></span>

### <span data-ttu-id="f3f96-129">AzureWebAppSnapshot (\*). i m App.</span><span class="sxs-lookup"><span data-stu-id="f3f96-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="f3f96-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f3f96-130">NOTES</span></span>

## <span data-ttu-id="f3f96-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3f96-131">RELATED LINKS</span></span>

