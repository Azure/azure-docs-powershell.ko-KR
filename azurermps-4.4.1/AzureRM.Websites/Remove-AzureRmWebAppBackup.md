---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: ba7255c41b5851b1f34b2ff7a1523c691925bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536895"
---
# <span data-ttu-id="44e8d-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="44e8d-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="44e8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44e8d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44e8d-103">구문과</span><span class="sxs-lookup"><span data-stu-id="44e8d-103">SYNTAX</span></span>

### <span data-ttu-id="44e8d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="44e8d-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44e8d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="44e8d-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44e8d-106">설명은</span><span class="sxs-lookup"><span data-stu-id="44e8d-106">DESCRIPTION</span></span>
<span data-ttu-id="44e8d-107">**AzureRmWebAppBackup** cmdlet은 지정 된 Azure Web App 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e8d-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="44e8d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="44e8d-108">EXAMPLES</span></span>

### <span data-ttu-id="44e8d-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="44e8d-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="44e8d-110">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 이라는 웹 앱에서 ID가 "12345" 인 백업을 사용 하 여 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e8d-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="44e8d-111">변수</span><span class="sxs-lookup"><span data-stu-id="44e8d-111">PARAMETERS</span></span>

### <span data-ttu-id="44e8d-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="44e8d-112">-BackupId</span></span>
<span data-ttu-id="44e8d-113">백업 Id</span><span class="sxs-lookup"><span data-stu-id="44e8d-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44e8d-114">-이름</span><span class="sxs-lookup"><span data-stu-id="44e8d-114">-Name</span></span>
<span data-ttu-id="44e8d-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="44e8d-115">WebApp Name</span></span>

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

### <span data-ttu-id="44e8d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44e8d-116">-ResourceGroupName</span></span>
<span data-ttu-id="44e8d-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="44e8d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="44e8d-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="44e8d-118">-Slot</span></span>
<span data-ttu-id="44e8d-119">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="44e8d-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="44e8d-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="44e8d-120">-WebApp</span></span>
<span data-ttu-id="44e8d-121">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="44e8d-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44e8d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e8d-122">-DefaultProfile</span></span>
<span data-ttu-id="44e8d-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44e8d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44e8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e8d-124">CommonParameters</span></span>
<span data-ttu-id="44e8d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e8d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44e8d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e8d-127">입력</span><span class="sxs-lookup"><span data-stu-id="44e8d-127">INPUTS</span></span>

### <span data-ttu-id="44e8d-128">Site</span><span class="sxs-lookup"><span data-stu-id="44e8d-128">Site</span></span>
<span data-ttu-id="44e8d-129">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44e8d-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="44e8d-130">출력</span><span class="sxs-lookup"><span data-stu-id="44e8d-130">OUTPUTS</span></span>

### <span data-ttu-id="44e8d-131">Microsoft. Azure. 관리자.</span><span class="sxs-lookup"><span data-stu-id="44e8d-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="44e8d-132">상속자</span><span class="sxs-lookup"><span data-stu-id="44e8d-132">NOTES</span></span>

## <span data-ttu-id="44e8d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44e8d-133">RELATED LINKS</span></span>

