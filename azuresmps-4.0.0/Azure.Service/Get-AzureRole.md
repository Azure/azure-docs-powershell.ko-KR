---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046314"
---
# <span data-ttu-id="c5f0c-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="c5f0c-101">Get-AzureRole</span></span>

## <span data-ttu-id="c5f0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f0c-103">Microsoft Azure 서비스의 역할 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="c5f0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5f0c-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5f0c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c5f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="c5f0c-106">**AzureRole** Cmdlet은 Microsoft Azure 서비스의 역할에 대 한 세부 정보를 포함 하는 list 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="c5f0c-107">*RoleName* 매개 변수를 지정 하는 경우 **Get-AzureRole** 는 해당 역할에 대 한 정보만 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="c5f0c-108">*Instancedetails* 매개 변수를 지정 하면 추가, 인스턴스 관련 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="c5f0c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c5f0c-109">EXAMPLES</span></span>

### <span data-ttu-id="c5f0c-110">예제 1: 서비스에 대 한 역할 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="c5f0c-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="c5f0c-111">이 명령은 MySvc01 서비스에서 실행 되는 모든 프로덕션 역할에 대 한 세부 정보가 포함 된 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="c5f0c-112">예제 2: 서비스에서 실행 되는 역할에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c5f0c-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="c5f0c-113">이 명령은 MyTestVM3 역할에 대 한 세부 정보가 포함 된 개체를 반환 하며, MySvc01 서비스의 스테이징 환경에서 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="c5f0c-114">예제 3: 서비스에서 실행 되는 역할의 인스턴스에 대 한 인스턴스 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c5f0c-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="c5f0c-115">이 명령은 MySvc01 서비스의 프로덕션 환경에서 실행 되는 MyTestVM02 역할의 인스턴스에 대 한 세부 정보가 포함 된 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="c5f0c-116">예제 4: 서비스와 연결 된 역할 인스턴스의 테이블 가져오기</span><span class="sxs-lookup"><span data-stu-id="c5f0c-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="c5f0c-117">이 명령은 MySvc01 서비스의 프로덕션 환경에서 실행 되는 모든 역할 인스턴스의 인스턴스 이름, 크기, 상태 테이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="c5f0c-118">변수</span><span class="sxs-lookup"><span data-stu-id="c5f0c-118">PARAMETERS</span></span>

### <span data-ttu-id="c5f0c-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c5f0c-119">-InformationAction</span></span>
<span data-ttu-id="c5f0c-120">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c5f0c-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c5f0c-122">하기로</span><span class="sxs-lookup"><span data-stu-id="c5f0c-122">Continue</span></span>
- <span data-ttu-id="c5f0c-123">숨기기</span><span class="sxs-lookup"><span data-stu-id="c5f0c-123">Ignore</span></span>
- <span data-ttu-id="c5f0c-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="c5f0c-124">Inquire</span></span>
- <span data-ttu-id="c5f0c-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c5f0c-125">SilentlyContinue</span></span>
- <span data-ttu-id="c5f0c-126">중지가</span><span class="sxs-lookup"><span data-stu-id="c5f0c-126">Stop</span></span>
- <span data-ttu-id="c5f0c-127">대기</span><span class="sxs-lookup"><span data-stu-id="c5f0c-127">Suspend</span></span>

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

### <span data-ttu-id="c5f0c-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c5f0c-128">-InformationVariable</span></span>
<span data-ttu-id="c5f0c-129">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c5f0c-130">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="c5f0c-130">-InstanceDetails</span></span>
<span data-ttu-id="c5f0c-131">이 cmdlet이 각 역할의 인스턴스에 대 한 세부 정보를 반환 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5f0c-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="c5f0c-132">-Profile</span></span>
<span data-ttu-id="c5f0c-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c5f0c-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c5f0c-135">-RoleName</span><span class="sxs-lookup"><span data-stu-id="c5f0c-135">-RoleName</span></span>
<span data-ttu-id="c5f0c-136">가져올 역할의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-136">Specifies the name of the role to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5f0c-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c5f0c-137">-ServiceName</span></span>
<span data-ttu-id="c5f0c-138">Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-138">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="c5f0c-139">-슬롯</span><span class="sxs-lookup"><span data-stu-id="c5f0c-139">-Slot</span></span>
<span data-ttu-id="c5f0c-140">Azure 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="c5f0c-141">이 매개 변수에 허용 되는 값은 프로덕션 또는 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-141">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5f0c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f0c-142">CommonParameters</span></span>
<span data-ttu-id="c5f0c-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5f0c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f0c-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5f0c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f0c-145">입력</span><span class="sxs-lookup"><span data-stu-id="c5f0c-145">INPUTS</span></span>

## <span data-ttu-id="c5f0c-146">출력</span><span class="sxs-lookup"><span data-stu-id="c5f0c-146">OUTPUTS</span></span>

## <span data-ttu-id="c5f0c-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c5f0c-147">NOTES</span></span>

## <span data-ttu-id="c5f0c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5f0c-148">RELATED LINKS</span></span>

[<span data-ttu-id="c5f0c-149">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="c5f0c-149">Set-AzureRole</span></span>](./Set-AzureRole.md)


