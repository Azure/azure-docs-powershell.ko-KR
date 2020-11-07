---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: fab46f997492c366857c7d13bea38543cca4e91c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698343"
---
# <span data-ttu-id="f79e7-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f79e7-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="f79e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f79e7-102">SYNOPSIS</span></span>
<span data-ttu-id="f79e7-103">웹 앱에 사용할 수 있는 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="f79e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f79e7-104">SYNTAX</span></span>

### <span data-ttu-id="f79e7-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f79e7-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f79e7-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f79e7-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f79e7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f79e7-107">DESCRIPTION</span></span>
<span data-ttu-id="f79e7-108">**AzWebAppSnapshot** cmdlet은 웹 앱에 대 한 모든 스냅숏을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="f79e7-109">스냅숏은 웹 앱의 파일 및 설정에 대 한 자동 백업입니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="f79e7-110">스냅숏은 **Restore-AzWebAppSnapshot** cmdlet을 사용 하 여 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="f79e7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f79e7-111">EXAMPLES</span></span>

### <span data-ttu-id="f79e7-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f79e7-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="f79e7-113">"기본-웹-WestUS" 리소스 그룹에서 "준비" 라는 슬롯을 사용 하 여 "ConstosoApp" 라는 웹 앱에 대 한 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="f79e7-114">변수</span><span class="sxs-lookup"><span data-stu-id="f79e7-114">PARAMETERS</span></span>

### <span data-ttu-id="f79e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79e7-115">-DefaultProfile</span></span>
<span data-ttu-id="f79e7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f79e7-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f79e7-117">-Name</span></span>
<span data-ttu-id="f79e7-118">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-118">The name of the web app.</span></span>

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

### <span data-ttu-id="f79e7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f79e7-119">-ResourceGroupName</span></span>
<span data-ttu-id="f79e7-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="f79e7-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="f79e7-121">-Slot</span></span>
<span data-ttu-id="f79e7-122">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="f79e7-123">-Web app</span><span class="sxs-lookup"><span data-stu-id="f79e7-123">-WebApp</span></span>
<span data-ttu-id="f79e7-124">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="f79e7-124">The web app object</span></span>

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

### <span data-ttu-id="f79e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79e7-125">CommonParameters</span></span>
<span data-ttu-id="f79e7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f79e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79e7-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f79e7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79e7-128">입력</span><span class="sxs-lookup"><span data-stu-id="f79e7-128">INPUTS</span></span>

### <span data-ttu-id="f79e7-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f79e7-129">System.String</span></span>

### <span data-ttu-id="f79e7-130">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="f79e7-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f79e7-131">출력</span><span class="sxs-lookup"><span data-stu-id="f79e7-131">OUTPUTS</span></span>

### <span data-ttu-id="f79e7-132">AzureWebAppSnapshot (\*). i m App.</span><span class="sxs-lookup"><span data-stu-id="f79e7-132">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="f79e7-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f79e7-133">NOTES</span></span>

## <span data-ttu-id="f79e7-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f79e7-134">RELATED LINKS</span></span>
