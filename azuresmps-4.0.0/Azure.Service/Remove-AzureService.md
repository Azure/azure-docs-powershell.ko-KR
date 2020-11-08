---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03107EA1-6ADA-4A3E-B8E1-88788E5F3F37
online version: ''
schema: 2.0.0
ms.openlocfilehash: 21892d129319977897a6855933e3e8542460a4a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046127"
---
# <span data-ttu-id="ae4e0-101">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="ae4e0-101">Remove-AzureService</span></span>

## <span data-ttu-id="ae4e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4e0-103">현재 클라우드 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-103">Removes the current cloud service.</span></span>

## <span data-ttu-id="ae4e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae4e0-104">SYNTAX</span></span>

```
Remove-AzureService [-ServiceName <String>] [-Force] [-PassThru] [-DeleteAll] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae4e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae4e0-105">DESCRIPTION</span></span>
<span data-ttu-id="ae4e0-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ae4e0-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ae4e0-108">**-Azureservice** cmdlet은 현재 클라우드 서비스를 중지 하 고 지정 된 서비스 및 구독 이름과 일치 하는 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-108">The **Remove-AzureService** cmdlet stops and removes the current cloud service, or the service matching the specified service and subscription name.</span></span>

## <span data-ttu-id="ae4e0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ae4e0-109">EXAMPLES</span></span>

## <span data-ttu-id="ae4e0-110">변수</span><span class="sxs-lookup"><span data-stu-id="ae4e0-110">PARAMETERS</span></span>

### <span data-ttu-id="ae4e0-111">-DeleteAll</span><span class="sxs-lookup"><span data-stu-id="ae4e0-111">-DeleteAll</span></span>
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

### <span data-ttu-id="ae4e0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="ae4e0-112">-Force</span></span>
<span data-ttu-id="ae4e0-113">확인 메시지를 표시 하지 않고 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-113">Removes the service without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ae4e0-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae4e0-114">-PassThru</span></span>
<span data-ttu-id="ae4e0-115">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ae4e0-116">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae4e0-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="ae4e0-117">-Profile</span></span>
<span data-ttu-id="ae4e0-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae4e0-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae4e0-120">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ae4e0-120">-ServiceName</span></span>
<span data-ttu-id="ae4e0-121">제거할 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-121">Specifies the name of the service to be removed.</span></span>
<span data-ttu-id="ae4e0-122">서비스 디렉터리에서 명령을 실행 하 고 이름을 지정 하지 않은 경우에는 현재 서비스 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-122">If the command is run from a service directory and no name is specified, uses the current service name.</span></span>

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

### <span data-ttu-id="ae4e0-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ae4e0-123">-Confirm</span></span>
<span data-ttu-id="ae4e0-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4e0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae4e0-125">-WhatIf</span></span>
<span data-ttu-id="ae4e0-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae4e0-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4e0-128">CommonParameters</span></span>
<span data-ttu-id="ae4e0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae4e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4e0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae4e0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4e0-131">입력</span><span class="sxs-lookup"><span data-stu-id="ae4e0-131">INPUTS</span></span>

## <span data-ttu-id="ae4e0-132">출력</span><span class="sxs-lookup"><span data-stu-id="ae4e0-132">OUTPUTS</span></span>

## <span data-ttu-id="ae4e0-133">상속자</span><span class="sxs-lookup"><span data-stu-id="ae4e0-133">NOTES</span></span>

## <span data-ttu-id="ae4e0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae4e0-134">RELATED LINKS</span></span>

[<span data-ttu-id="ae4e0-135">게시-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ae4e0-135">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="ae4e0-136">정지-AzureService</span><span class="sxs-lookup"><span data-stu-id="ae4e0-136">Stop-AzureService</span></span>](./Stop-AzureService.md)

[<span data-ttu-id="ae4e0-137">시작-AzureService</span><span class="sxs-lookup"><span data-stu-id="ae4e0-137">Start-AzureService</span></span>](./Start-AzureService.md)


