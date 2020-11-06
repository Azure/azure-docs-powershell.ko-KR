---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 75c134b162636f94b00cf6692f4e9df120930dcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530808"
---
# <span data-ttu-id="67a52-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="67a52-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="67a52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a52-102">SYNOPSIS</span></span>
<span data-ttu-id="67a52-103">웹 앱 슬롯 구성 이름 설정</span><span class="sxs-lookup"><span data-stu-id="67a52-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67a52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67a52-104">SYNTAX</span></span>

### <span data-ttu-id="67a52-105">S1</span><span class="sxs-lookup"><span data-stu-id="67a52-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67a52-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="67a52-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67a52-107">설명은</span><span class="sxs-lookup"><span data-stu-id="67a52-107">DESCRIPTION</span></span>
<span data-ttu-id="67a52-108">**Set-AzureRmWebAppSlotConfigName** Cmdlet은 앱 설정 및 연결 문자열을 슬롯 설정으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a52-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="67a52-109">예제의</span><span class="sxs-lookup"><span data-stu-id="67a52-109">EXAMPLES</span></span>

### <span data-ttu-id="67a52-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="67a52-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="67a52-111">이 명령은 리소스 그룹 ContosoWebApp에 연결 된 웹 앱에 대 한 모든 앱 설정 및 연결 문자열을 제거 합니다. 기본값-웹-WestUS</span><span class="sxs-lookup"><span data-stu-id="67a52-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="67a52-112">변수</span><span class="sxs-lookup"><span data-stu-id="67a52-112">PARAMETERS</span></span>

### <span data-ttu-id="67a52-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="67a52-113">-AppSettingNames</span></span>
<span data-ttu-id="67a52-114">앱 설정 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="67a52-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a52-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="67a52-115">-ConnectionStringNames</span></span>
<span data-ttu-id="67a52-116">연결 문자열 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="67a52-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a52-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a52-117">-DefaultProfile</span></span>
<span data-ttu-id="67a52-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67a52-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67a52-119">-이름</span><span class="sxs-lookup"><span data-stu-id="67a52-119">-Name</span></span>
<span data-ttu-id="67a52-120">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="67a52-120">WebApp Name</span></span>

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

### <span data-ttu-id="67a52-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="67a52-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="67a52-122">모든 앱 설정 이름 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="67a52-122">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a52-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="67a52-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="67a52-124">모든 연결 문자열 이름 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="67a52-124">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67a52-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a52-125">-ResourceGroupName</span></span>
<span data-ttu-id="67a52-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="67a52-126">Resource Group Name</span></span>

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

### <span data-ttu-id="67a52-127">-Web app</span><span class="sxs-lookup"><span data-stu-id="67a52-127">-WebApp</span></span>
<span data-ttu-id="67a52-128">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="67a52-128">WebApp Object</span></span>

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

### <span data-ttu-id="67a52-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a52-129">CommonParameters</span></span>
<span data-ttu-id="67a52-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67a52-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a52-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a52-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a52-132">입력</span><span class="sxs-lookup"><span data-stu-id="67a52-132">INPUTS</span></span>

### <span data-ttu-id="67a52-133">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="67a52-133">System.String[]</span></span>

### <span data-ttu-id="67a52-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67a52-134">System.String</span></span>

### <span data-ttu-id="67a52-135">Microsoft. Azure. 사이트</span><span class="sxs-lookup"><span data-stu-id="67a52-135">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="67a52-136">매개 변수: Web app (ByValue)</span><span class="sxs-lookup"><span data-stu-id="67a52-136">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="67a52-137">출력</span><span class="sxs-lookup"><span data-stu-id="67a52-137">OUTPUTS</span></span>

### <span data-ttu-id="67a52-138">SlotConfigNamesResource/. m i.</span><span class="sxs-lookup"><span data-stu-id="67a52-138">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="67a52-139">상속자</span><span class="sxs-lookup"><span data-stu-id="67a52-139">NOTES</span></span>

## <span data-ttu-id="67a52-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67a52-140">RELATED LINKS</span></span>
