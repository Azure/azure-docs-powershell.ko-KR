---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045824"
---
# <span data-ttu-id="feddf-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="feddf-101">Set-AzureRole</span></span>

## <span data-ttu-id="feddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feddf-102">SYNOPSIS</span></span>
<span data-ttu-id="feddf-103">실행할 Azure 역할의 인스턴스 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="feddf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="feddf-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="feddf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="feddf-105">DESCRIPTION</span></span>
<span data-ttu-id="feddf-106">**AzureRole** Cmdlet은 Azure 배포에서 실행할 지정 된 역할의 인스턴스 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="feddf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="feddf-107">EXAMPLES</span></span>

### <span data-ttu-id="feddf-108">1: 역할의 인스턴스 수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="feddf-109">이 명령은 MySvc01 서비스에서 프로덕션으로 실행 되는 MyTestRole03 역할을 세 가지 인스턴스로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="feddf-110">변수</span><span class="sxs-lookup"><span data-stu-id="feddf-110">PARAMETERS</span></span>

### <span data-ttu-id="feddf-111">-카운트</span><span class="sxs-lookup"><span data-stu-id="feddf-111">-Count</span></span>
<span data-ttu-id="feddf-112">실행할 역할 인스턴스의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feddf-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="feddf-113">-InformationAction</span></span>
<span data-ttu-id="feddf-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="feddf-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="feddf-116">하기로</span><span class="sxs-lookup"><span data-stu-id="feddf-116">Continue</span></span>
- <span data-ttu-id="feddf-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="feddf-117">Ignore</span></span>
- <span data-ttu-id="feddf-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="feddf-118">Inquire</span></span>
- <span data-ttu-id="feddf-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="feddf-119">SilentlyContinue</span></span>
- <span data-ttu-id="feddf-120">중지가</span><span class="sxs-lookup"><span data-stu-id="feddf-120">Stop</span></span>
- <span data-ttu-id="feddf-121">대기</span><span class="sxs-lookup"><span data-stu-id="feddf-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feddf-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="feddf-122">-InformationVariable</span></span>
<span data-ttu-id="feddf-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feddf-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="feddf-124">-Profile</span></span>
<span data-ttu-id="feddf-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="feddf-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="feddf-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="feddf-127">-RoleName</span></span>
<span data-ttu-id="feddf-128">인스턴스 수를 설정할 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-128">Specifies the name of the role for which to set the number of instances.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feddf-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="feddf-129">-ServiceName</span></span>
<span data-ttu-id="feddf-130">Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-130">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feddf-131">-슬롯</span><span class="sxs-lookup"><span data-stu-id="feddf-131">-Slot</span></span>
<span data-ttu-id="feddf-132">수정할 배포의 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="feddf-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="feddf-134">프로덕션용</span><span class="sxs-lookup"><span data-stu-id="feddf-134">Production</span></span>
- <span data-ttu-id="feddf-135">대기</span><span class="sxs-lookup"><span data-stu-id="feddf-135">Staging</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="feddf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feddf-136">CommonParameters</span></span>
<span data-ttu-id="feddf-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="feddf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feddf-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feddf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feddf-139">입력</span><span class="sxs-lookup"><span data-stu-id="feddf-139">INPUTS</span></span>

## <span data-ttu-id="feddf-140">출력</span><span class="sxs-lookup"><span data-stu-id="feddf-140">OUTPUTS</span></span>

## <span data-ttu-id="feddf-141">상속자</span><span class="sxs-lookup"><span data-stu-id="feddf-141">NOTES</span></span>

## <span data-ttu-id="feddf-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="feddf-142">RELATED LINKS</span></span>

[<span data-ttu-id="feddf-143">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="feddf-143">Get-AzureRole</span></span>](./Get-AzureRole.md)


