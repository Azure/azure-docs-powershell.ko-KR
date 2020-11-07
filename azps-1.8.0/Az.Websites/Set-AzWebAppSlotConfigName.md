---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: 5e2b13cd4c2586b15cc526aad3d922441b40265c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698292"
---
# <span data-ttu-id="81ba5-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="81ba5-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="81ba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="81ba5-103">웹 앱 슬롯 구성 이름 설정</span><span class="sxs-lookup"><span data-stu-id="81ba5-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="81ba5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81ba5-104">SYNTAX</span></span>

### <span data-ttu-id="81ba5-105">S1</span><span class="sxs-lookup"><span data-stu-id="81ba5-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81ba5-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="81ba5-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81ba5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="81ba5-107">DESCRIPTION</span></span>
<span data-ttu-id="81ba5-108">**Set-AzWebAppSlotConfigName** Cmdlet은 앱 설정 및 연결 문자열을 슬롯 설정으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="81ba5-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="81ba5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="81ba5-109">EXAMPLES</span></span>

### <span data-ttu-id="81ba5-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="81ba5-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="81ba5-111">이 명령은 리소스 그룹 ContosoWebApp에 연결 된 웹 앱에 대 한 모든 앱 설정 및 연결 문자열을 제거 합니다. 기본값-웹-WestUS</span><span class="sxs-lookup"><span data-stu-id="81ba5-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="81ba5-112">변수</span><span class="sxs-lookup"><span data-stu-id="81ba5-112">PARAMETERS</span></span>

### <span data-ttu-id="81ba5-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="81ba5-113">-AppSettingNames</span></span>
<span data-ttu-id="81ba5-114">앱 설정 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="81ba5-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="81ba5-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="81ba5-115">-ConnectionStringNames</span></span>
<span data-ttu-id="81ba5-116">연결 문자열 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="81ba5-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="81ba5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ba5-117">-DefaultProfile</span></span>
<span data-ttu-id="81ba5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81ba5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81ba5-119">-이름</span><span class="sxs-lookup"><span data-stu-id="81ba5-119">-Name</span></span>
<span data-ttu-id="81ba5-120">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="81ba5-120">WebApp Name</span></span>

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

### <span data-ttu-id="81ba5-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="81ba5-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="81ba5-122">모든 앱 설정 이름 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="81ba5-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="81ba5-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="81ba5-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="81ba5-124">모든 연결 문자열 이름 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="81ba5-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="81ba5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81ba5-125">-ResourceGroupName</span></span>
<span data-ttu-id="81ba5-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="81ba5-126">Resource Group Name</span></span>

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

### <span data-ttu-id="81ba5-127">-Web app</span><span class="sxs-lookup"><span data-stu-id="81ba5-127">-WebApp</span></span>
<span data-ttu-id="81ba5-128">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="81ba5-128">WebApp Object</span></span>

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

### <span data-ttu-id="81ba5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ba5-129">CommonParameters</span></span>
<span data-ttu-id="81ba5-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81ba5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ba5-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81ba5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ba5-132">입력</span><span class="sxs-lookup"><span data-stu-id="81ba5-132">INPUTS</span></span>

### <span data-ttu-id="81ba5-133">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="81ba5-133">System.String[]</span></span>

### <span data-ttu-id="81ba5-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="81ba5-134">System.String</span></span>

### <span data-ttu-id="81ba5-135">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="81ba5-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="81ba5-136">출력</span><span class="sxs-lookup"><span data-stu-id="81ba5-136">OUTPUTS</span></span>

### <span data-ttu-id="81ba5-137">SlotConfigNamesResource/. m i.</span><span class="sxs-lookup"><span data-stu-id="81ba5-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="81ba5-138">상속자</span><span class="sxs-lookup"><span data-stu-id="81ba5-138">NOTES</span></span>

## <span data-ttu-id="81ba5-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81ba5-139">RELATED LINKS</span></span>
