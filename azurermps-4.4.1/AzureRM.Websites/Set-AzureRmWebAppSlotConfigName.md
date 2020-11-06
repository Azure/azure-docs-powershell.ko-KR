---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 3ed7bd25c394c2bef5cb3636a4f8c238f45a3558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525444"
---
# <span data-ttu-id="13ca8-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="13ca8-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="13ca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="13ca8-103">웹 앱 슬롯 구성 이름 설정</span><span class="sxs-lookup"><span data-stu-id="13ca8-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13ca8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13ca8-104">SYNTAX</span></span>

### <span data-ttu-id="13ca8-105">S1</span><span class="sxs-lookup"><span data-stu-id="13ca8-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ca8-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="13ca8-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13ca8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="13ca8-107">DESCRIPTION</span></span>
<span data-ttu-id="13ca8-108">**Set-AzureRmWebAppSlotConfigName** Cmdlet은 앱 설정 및 연결 문자열을 슬롯 설정으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13ca8-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="13ca8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="13ca8-109">EXAMPLES</span></span>

### <span data-ttu-id="13ca8-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="13ca8-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="13ca8-111">이 명령은 리소스 그룹 ContosoWebApp에 연결 된 웹 앱에 대 한 모든 앱 설정 및 연결 문자열을 제거 합니다. 기본값-웹-WestUS</span><span class="sxs-lookup"><span data-stu-id="13ca8-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="13ca8-112">변수</span><span class="sxs-lookup"><span data-stu-id="13ca8-112">PARAMETERS</span></span>

### <span data-ttu-id="13ca8-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="13ca8-113">-AppSettingNames</span></span>
<span data-ttu-id="13ca8-114">앱 설정 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="13ca8-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="13ca8-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="13ca8-115">-ConnectionStringNames</span></span>
<span data-ttu-id="13ca8-116">연결 문자열 이름 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="13ca8-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="13ca8-117">-이름</span><span class="sxs-lookup"><span data-stu-id="13ca8-117">-Name</span></span>
<span data-ttu-id="13ca8-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="13ca8-118">WebApp Name</span></span>

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

### <span data-ttu-id="13ca8-119">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="13ca8-119">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="13ca8-120">모든 앱 설정 이름 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="13ca8-120">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="13ca8-121">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="13ca8-121">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="13ca8-122">모든 연결 문자열 이름 제거 옵션</span><span class="sxs-lookup"><span data-stu-id="13ca8-122">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="13ca8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ca8-123">-ResourceGroupName</span></span>
<span data-ttu-id="13ca8-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="13ca8-124">Resource Group Name</span></span>

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

### <span data-ttu-id="13ca8-125">-Web app</span><span class="sxs-lookup"><span data-stu-id="13ca8-125">-WebApp</span></span>
<span data-ttu-id="13ca8-126">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="13ca8-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13ca8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ca8-127">-DefaultProfile</span></span>
<span data-ttu-id="13ca8-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13ca8-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13ca8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ca8-129">CommonParameters</span></span>
<span data-ttu-id="13ca8-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13ca8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ca8-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13ca8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ca8-132">입력</span><span class="sxs-lookup"><span data-stu-id="13ca8-132">INPUTS</span></span>

### <span data-ttu-id="13ca8-133">Site</span><span class="sxs-lookup"><span data-stu-id="13ca8-133">Site</span></span>
<span data-ttu-id="13ca8-134">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="13ca8-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="13ca8-135">출력</span><span class="sxs-lookup"><span data-stu-id="13ca8-135">OUTPUTS</span></span>

## <span data-ttu-id="13ca8-136">상속자</span><span class="sxs-lookup"><span data-stu-id="13ca8-136">NOTES</span></span>

## <span data-ttu-id="13ca8-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13ca8-137">RELATED LINKS</span></span>

