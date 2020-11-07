---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: d16d9f515544e50cc973b0bb6d5e7fc2455f8a42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869526"
---
# <span data-ttu-id="1f428-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="1f428-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="1f428-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f428-102">SYNOPSIS</span></span>
<span data-ttu-id="1f428-103">웹 앱에 사용할 수 있는 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="1f428-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f428-104">SYNTAX</span></span>

### <span data-ttu-id="1f428-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1f428-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f428-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1f428-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f428-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1f428-107">DESCRIPTION</span></span>
<span data-ttu-id="1f428-108">**AzWebAppSnapshot** cmdlet은 웹 앱에 대 한 모든 스냅숏을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="1f428-109">스냅숏은 웹 앱의 파일 및 설정에 대 한 자동 백업입니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="1f428-110">스냅숏은 **Restore-AzWebAppSnapshot** cmdlet을 사용 하 여 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="1f428-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1f428-111">EXAMPLES</span></span>

### <span data-ttu-id="1f428-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f428-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="1f428-113">"기본-웹-WestUS" 리소스 그룹에서 "준비" 라는 슬롯을 사용 하 여 "ContosoApp" 라는 웹 앱에 대 한 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="1f428-114">변수</span><span class="sxs-lookup"><span data-stu-id="1f428-114">PARAMETERS</span></span>

### <span data-ttu-id="1f428-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f428-115">-DefaultProfile</span></span>
<span data-ttu-id="1f428-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f428-117">-이름</span><span class="sxs-lookup"><span data-stu-id="1f428-117">-Name</span></span>
<span data-ttu-id="1f428-118">웹 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-118">The name of the web app.</span></span>

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

### <span data-ttu-id="1f428-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f428-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f428-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f428-121">-슬롯</span><span class="sxs-lookup"><span data-stu-id="1f428-121">-Slot</span></span>
<span data-ttu-id="1f428-122">웹 앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="1f428-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="1f428-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="1f428-124">보조 눈금 단위에서 스냅숏을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-124">Read the snapshots from a secondary scale unit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f428-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="1f428-125">-WebApp</span></span>
<span data-ttu-id="1f428-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="1f428-126">The web app object</span></span>

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

### <span data-ttu-id="1f428-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f428-127">CommonParameters</span></span>
<span data-ttu-id="1f428-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f428-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f428-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f428-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f428-130">입력</span><span class="sxs-lookup"><span data-stu-id="1f428-130">INPUTS</span></span>

### <span data-ttu-id="1f428-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f428-131">System.String</span></span>

### <span data-ttu-id="1f428-132">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="1f428-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1f428-133">출력</span><span class="sxs-lookup"><span data-stu-id="1f428-133">OUTPUTS</span></span>

### <span data-ttu-id="1f428-134">AzureWebAppSnapshot (\*). i m App.</span><span class="sxs-lookup"><span data-stu-id="1f428-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="1f428-135">상속자</span><span class="sxs-lookup"><span data-stu-id="1f428-135">NOTES</span></span>

## <span data-ttu-id="1f428-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f428-136">RELATED LINKS</span></span>
