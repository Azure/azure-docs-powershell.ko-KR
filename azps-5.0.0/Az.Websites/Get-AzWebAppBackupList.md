---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 6ea805f1e3a3711c2efe6faefd73edf06c4b51fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309373"
---
# <span data-ttu-id="f619d-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="f619d-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="f619d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f619d-102">SYNOPSIS</span></span>

## <span data-ttu-id="f619d-103">구문과</span><span class="sxs-lookup"><span data-stu-id="f619d-103">SYNTAX</span></span>

### <span data-ttu-id="f619d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f619d-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f619d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f619d-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f619d-106">설명은</span><span class="sxs-lookup"><span data-stu-id="f619d-106">DESCRIPTION</span></span>
<span data-ttu-id="f619d-107">**AzWebAppBackupList** Cmdlet은 Azure Web App에 대 한 백업 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f619d-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="f619d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f619d-108">EXAMPLES</span></span>

### <span data-ttu-id="f619d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f619d-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="f619d-110">이 명령은 리소스 그룹 ContosoResourceGroup 연결 된 Web app WebAppStandard와 관련 된 백업 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f619d-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="f619d-111">변수</span><span class="sxs-lookup"><span data-stu-id="f619d-111">PARAMETERS</span></span>

### <span data-ttu-id="f619d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f619d-112">-DefaultProfile</span></span>
<span data-ttu-id="f619d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f619d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f619d-114">-이름</span><span class="sxs-lookup"><span data-stu-id="f619d-114">-Name</span></span>
<span data-ttu-id="f619d-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="f619d-115">WebApp Name</span></span>

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

### <span data-ttu-id="f619d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f619d-116">-ResourceGroupName</span></span>
<span data-ttu-id="f619d-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f619d-117">Resource Group Name</span></span>

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

### <span data-ttu-id="f619d-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="f619d-118">-Slot</span></span>
<span data-ttu-id="f619d-119">슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="f619d-119">Slot name</span></span>

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

### <span data-ttu-id="f619d-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="f619d-120">-WebApp</span></span>
<span data-ttu-id="f619d-121">파이프 Web app</span><span class="sxs-lookup"><span data-stu-id="f619d-121">Piped WebApp</span></span>

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

### <span data-ttu-id="f619d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f619d-122">CommonParameters</span></span>
<span data-ttu-id="f619d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f619d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f619d-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f619d-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f619d-125">입력</span><span class="sxs-lookup"><span data-stu-id="f619d-125">INPUTS</span></span>

### <span data-ttu-id="f619d-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f619d-126">System.String</span></span>

### <span data-ttu-id="f619d-127">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="f619d-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f619d-128">출력</span><span class="sxs-lookup"><span data-stu-id="f619d-128">OUTPUTS</span></span>

### <span data-ttu-id="f619d-129">AzureWebAppBackup (\*). WebApps.</span><span class="sxs-lookup"><span data-stu-id="f619d-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="f619d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f619d-130">NOTES</span></span>

## <span data-ttu-id="f619d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f619d-131">RELATED LINKS</span></span>
