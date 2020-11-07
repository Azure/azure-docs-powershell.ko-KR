---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: b533d63e83d731dd5b95788609d32fa4cf7863f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876160"
---
# <span data-ttu-id="41f3b-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="41f3b-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="41f3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41f3b-102">SYNOPSIS</span></span>

## <span data-ttu-id="41f3b-103">구문과</span><span class="sxs-lookup"><span data-stu-id="41f3b-103">SYNTAX</span></span>

### <span data-ttu-id="41f3b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="41f3b-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41f3b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="41f3b-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41f3b-106">설명은</span><span class="sxs-lookup"><span data-stu-id="41f3b-106">DESCRIPTION</span></span>
<span data-ttu-id="41f3b-107">**AzWebAppBackup** cmdlet은 지정 된 Azure Web App 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41f3b-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="41f3b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="41f3b-108">EXAMPLES</span></span>

### <span data-ttu-id="41f3b-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="41f3b-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="41f3b-110">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 이라는 웹 앱에서 ID가 "12345" 인 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41f3b-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="41f3b-111">변수</span><span class="sxs-lookup"><span data-stu-id="41f3b-111">PARAMETERS</span></span>

### <span data-ttu-id="41f3b-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="41f3b-112">-BackupId</span></span>
<span data-ttu-id="41f3b-113">백업 Id</span><span class="sxs-lookup"><span data-stu-id="41f3b-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f3b-114">-DefaultProfile</span></span>
<span data-ttu-id="41f3b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41f3b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f3b-116">-이름</span><span class="sxs-lookup"><span data-stu-id="41f3b-116">-Name</span></span>
<span data-ttu-id="41f3b-117">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="41f3b-117">Webapp Name</span></span>

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

### <span data-ttu-id="41f3b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f3b-118">-ResourceGroupName</span></span>
<span data-ttu-id="41f3b-119">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="41f3b-119">Resource Group Name</span></span>

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

### <span data-ttu-id="41f3b-120">-슬롯</span><span class="sxs-lookup"><span data-stu-id="41f3b-120">-Slot</span></span>
<span data-ttu-id="41f3b-121">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="41f3b-121">Slot Name</span></span>

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

### <span data-ttu-id="41f3b-122">-Web app</span><span class="sxs-lookup"><span data-stu-id="41f3b-122">-WebApp</span></span>
<span data-ttu-id="41f3b-123">파이프 Web app</span><span class="sxs-lookup"><span data-stu-id="41f3b-123">Piped WebApp</span></span>

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

### <span data-ttu-id="41f3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f3b-124">CommonParameters</span></span>
<span data-ttu-id="41f3b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f3b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f3b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f3b-127">입력</span><span class="sxs-lookup"><span data-stu-id="41f3b-127">INPUTS</span></span>

### <span data-ttu-id="41f3b-128">Site</span><span class="sxs-lookup"><span data-stu-id="41f3b-128">Site</span></span>
<span data-ttu-id="41f3b-129">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="41f3b-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="41f3b-130">출력</span><span class="sxs-lookup"><span data-stu-id="41f3b-130">OUTPUTS</span></span>

### <span data-ttu-id="41f3b-131">AzureWebAppBackup (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="41f3b-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="41f3b-132">상속자</span><span class="sxs-lookup"><span data-stu-id="41f3b-132">NOTES</span></span>

## <span data-ttu-id="41f3b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41f3b-133">RELATED LINKS</span></span>

