---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D15329E9-BB72-4F1B-B79A-E7AD920A9D5A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92c972bb693a1e13b365635064785182c53af409
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046509"
---
# <span data-ttu-id="1bba2-101">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="1bba2-101">Get-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="1bba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bba2-102">SYNOPSIS</span></span>
<span data-ttu-id="1bba2-103">웹 사이트 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-103">Gets the deployments for a website.</span></span>

## <span data-ttu-id="1bba2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1bba2-104">SYNTAX</span></span>

```
Get-AzureWebsiteDeployment [-CommitId <String>] [-MaxResults <Int32>] [-Details] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1bba2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1bba2-105">DESCRIPTION</span></span>
<span data-ttu-id="1bba2-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1bba2-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1bba2-108">Azure의 웹 사이트 배포를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-108">Gets the deployments for a website in Azure.</span></span>

## <span data-ttu-id="1bba2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1bba2-109">EXAMPLES</span></span>

## <span data-ttu-id="1bba2-110">변수</span><span class="sxs-lookup"><span data-stu-id="1bba2-110">PARAMETERS</span></span>

### <span data-ttu-id="1bba2-111">-CommitId</span><span class="sxs-lookup"><span data-stu-id="1bba2-111">-CommitId</span></span>
<span data-ttu-id="1bba2-112">배포의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-112">Specifies the unique ID for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bba2-113">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="1bba2-113">-Details</span></span>
<span data-ttu-id="1bba2-114">배포에 대 한 자세한 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-114">Shows detailed information about the deployments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bba2-115">-MaxResults</span><span class="sxs-lookup"><span data-stu-id="1bba2-115">-MaxResults</span></span>
<span data-ttu-id="1bba2-116">명령으로 반환할 최대 결과 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-116">Specifies the largest number of results that you want the command to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bba2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="1bba2-117">-Name</span></span>
<span data-ttu-id="1bba2-118">배포 정보를 가져오려는 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-118">Specifies the name of the website for which you want to get deployment information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bba2-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="1bba2-119">-Profile</span></span>
<span data-ttu-id="1bba2-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1bba2-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bba2-122">-슬롯</span><span class="sxs-lookup"><span data-stu-id="1bba2-122">-Slot</span></span>
<span data-ttu-id="1bba2-123">슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-123">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bba2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bba2-124">CommonParameters</span></span>
<span data-ttu-id="1bba2-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bba2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bba2-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bba2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bba2-127">입력</span><span class="sxs-lookup"><span data-stu-id="1bba2-127">INPUTS</span></span>

## <span data-ttu-id="1bba2-128">출력</span><span class="sxs-lookup"><span data-stu-id="1bba2-128">OUTPUTS</span></span>

## <span data-ttu-id="1bba2-129">상속자</span><span class="sxs-lookup"><span data-stu-id="1bba2-129">NOTES</span></span>

## <span data-ttu-id="1bba2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bba2-130">RELATED LINKS</span></span>

[<span data-ttu-id="1bba2-131">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="1bba2-131">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


