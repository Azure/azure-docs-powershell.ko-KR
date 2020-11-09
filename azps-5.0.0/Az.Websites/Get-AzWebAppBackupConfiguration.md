---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308483"
---
# <span data-ttu-id="fdb3b-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="fdb3b-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="fdb3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdb3b-102">SYNOPSIS</span></span>

## <span data-ttu-id="fdb3b-103">구문과</span><span class="sxs-lookup"><span data-stu-id="fdb3b-103">SYNTAX</span></span>

### <span data-ttu-id="fdb3b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="fdb3b-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdb3b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="fdb3b-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fdb3b-106">설명은</span><span class="sxs-lookup"><span data-stu-id="fdb3b-106">DESCRIPTION</span></span>
<span data-ttu-id="fdb3b-107">**AzWebAppBackupConfiguration** Cmdlet은 Azure Web App의 백업 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fdb3b-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="fdb3b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fdb3b-108">EXAMPLES</span></span>

### <span data-ttu-id="fdb3b-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="fdb3b-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="fdb3b-110">이 명령은 리소스 그룹 Default-웹용 WestUS에 속한 WebAppStandard 이라는 웹 앱에서 백업 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fdb3b-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="fdb3b-111">변수</span><span class="sxs-lookup"><span data-stu-id="fdb3b-111">PARAMETERS</span></span>

### <span data-ttu-id="fdb3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb3b-112">-DefaultProfile</span></span>
<span data-ttu-id="fdb3b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb3b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdb3b-114">-이름</span><span class="sxs-lookup"><span data-stu-id="fdb3b-114">-Name</span></span>
<span data-ttu-id="fdb3b-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="fdb3b-115">WebApp Name</span></span>

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

### <span data-ttu-id="fdb3b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb3b-116">-ResourceGroupName</span></span>
<span data-ttu-id="fdb3b-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fdb3b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="fdb3b-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="fdb3b-118">-Slot</span></span>
<span data-ttu-id="fdb3b-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="fdb3b-119">Slot Name</span></span>

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

### <span data-ttu-id="fdb3b-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="fdb3b-120">-WebApp</span></span>
<span data-ttu-id="fdb3b-121">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="fdb3b-121">WebApp Name</span></span>

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

### <span data-ttu-id="fdb3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb3b-122">CommonParameters</span></span>
<span data-ttu-id="fdb3b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb3b-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb3b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb3b-125">입력</span><span class="sxs-lookup"><span data-stu-id="fdb3b-125">INPUTS</span></span>

### <span data-ttu-id="fdb3b-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fdb3b-126">System.String</span></span>

### <span data-ttu-id="fdb3b-127">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="fdb3b-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fdb3b-128">출력</span><span class="sxs-lookup"><span data-stu-id="fdb3b-128">OUTPUTS</span></span>

### <span data-ttu-id="fdb3b-129">AzureWebAppBackupConfiguration (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="fdb3b-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="fdb3b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="fdb3b-130">NOTES</span></span>

## <span data-ttu-id="fdb3b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdb3b-131">RELATED LINKS</span></span>
