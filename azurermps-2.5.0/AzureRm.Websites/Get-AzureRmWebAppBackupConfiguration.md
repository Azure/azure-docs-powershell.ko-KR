---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 67bf9eb23318e4771c00760d18a5659526c5f45a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880850"
---
# <span data-ttu-id="da828-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="da828-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="da828-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da828-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da828-103">구문과</span><span class="sxs-lookup"><span data-stu-id="da828-103">SYNTAX</span></span>

### <span data-ttu-id="da828-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="da828-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da828-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="da828-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da828-106">설명은</span><span class="sxs-lookup"><span data-stu-id="da828-106">DESCRIPTION</span></span>
<span data-ttu-id="da828-107">**AzureRmWebAppBackupConfiguration** Cmdlet은 Azure Web App의 백업 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da828-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="da828-108">예제의</span><span class="sxs-lookup"><span data-stu-id="da828-108">EXAMPLES</span></span>

### <span data-ttu-id="da828-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="da828-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="da828-110">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 이라는 웹 앱에서 백업 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="da828-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="da828-111">변수</span><span class="sxs-lookup"><span data-stu-id="da828-111">PARAMETERS</span></span>

### <span data-ttu-id="da828-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da828-112">-DefaultProfile</span></span>
<span data-ttu-id="da828-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da828-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da828-114">-이름</span><span class="sxs-lookup"><span data-stu-id="da828-114">-Name</span></span>
<span data-ttu-id="da828-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="da828-115">WebApp Name</span></span>

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

### <span data-ttu-id="da828-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da828-116">-ResourceGroupName</span></span>
<span data-ttu-id="da828-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="da828-117">Resource Group Name</span></span>

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

### <span data-ttu-id="da828-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="da828-118">-Slot</span></span>
<span data-ttu-id="da828-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="da828-119">Slot Name</span></span>

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

### <span data-ttu-id="da828-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="da828-120">-WebApp</span></span>
<span data-ttu-id="da828-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="da828-121">WebApp Name</span></span>

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

### <span data-ttu-id="da828-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da828-122">CommonParameters</span></span>
<span data-ttu-id="da828-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da828-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da828-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da828-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da828-125">입력</span><span class="sxs-lookup"><span data-stu-id="da828-125">INPUTS</span></span>

### <span data-ttu-id="da828-126">Site</span><span class="sxs-lookup"><span data-stu-id="da828-126">Site</span></span>
<span data-ttu-id="da828-127">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da828-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="da828-128">출력</span><span class="sxs-lookup"><span data-stu-id="da828-128">OUTPUTS</span></span>

### <span data-ttu-id="da828-129">AzureWebAppBackupConfiguration (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="da828-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="da828-130">상속자</span><span class="sxs-lookup"><span data-stu-id="da828-130">NOTES</span></span>

## <span data-ttu-id="da828-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da828-131">RELATED LINKS</span></span>

